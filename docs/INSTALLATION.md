# UntitleXTool Installation, Activation, and Release Guide

## English

### 1. Supported Packages

This is the `v1.0.0.0-beta` pre-release build for Windows. Each Maya version has its own installation package because Maya versions use different Python runtimes and compiled bytecode.

| Maya | Python Runtime | Package |
| --- | --- | --- |
| Maya 2022 | Python 3.7 | [Download ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip) |
| Maya 2023 | Python 3.9 | [Download ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2023_pyc.zip) |
| Maya 2024 | Python 3.10 | [Download ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip) |
| Maya 2025 | Python 3.11 | [Download ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2025_pyc.zip) |
| Maya 2026 | Python 3.11 | [Download ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2026_pyc.zip) |

Do not install a package intended for another Maya version.

### 2. Package Verification

Run the following command in PowerShell after downloading a package:

```powershell
Get-FileHash -Algorithm SHA256 .\UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip
```

Replace the filename for your Maya version and compare the result below:

| Maya | SHA-256 |
| --- | --- |
| Maya 2022 | `026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4` |
| Maya 2023 | `8DCDC49E01B959ABDF68FE53F00E9A741898C0AF25D1E8360689325AD78C0F5C` |
| Maya 2024 | `328537018E35B23C64CFA8191022511240D8CA304F0C3AE747EF5AB717DA16CF` |
| Maya 2025 | `70ABB43F6FAD6160E645B1D01CB30A02AF023C00DFF4C5D58C1166F259537BC3` |
| Maya 2026 | `48F5D395B9C8AEDAE20ADF1171A86863561A360A7F702C928DC656FCDEF4EFD0` |

Do not install a file whose hash does not match.

### 3. Installation

1. Download the ZIP matching your Maya version and fully extract it to a local folder.
2. Confirm the extracted directory contains both `install.py` and the `UntitleXTool` folder.
3. Start the corresponding Autodesk Maya version.
4. Drag `install.py` into the Maya main window or viewport.
5. Confirm the detected Maya version and user scripts directory, then click `Install / Update`.
6. Open `UntitleXTool WorkBench` from the `UntitleTool` shelf.

Expected extracted structure:

```text
UntitleXTool_<version>_Maya<year>_pyc/
|-- install.py
|-- README.txt
`-- UntitleXTool/
    |-- load.pyc
    |-- main.pyc
    |-- uninstall.pyc
    `-- ...
```

Keep `install.py` beside the full `UntitleXTool` folder. Do not run it directly from a ZIP preview.

### 4. License, Updating, and Removal

To activate licensed features, open `Settings > Plugin Settings > License` in WorkBench, enter the License Key received after purchase, and click `Activate`. Never include a License Key or `.lic` file in public screenshots or issues.

For an update, download the newest Release asset for the same Maya version and run its `install.py` again. The installer backs up the installed tool directory before replacement.

To uninstall, use the removal action in the `UntitleTool` shelf and restart Maya when complete. Back up custom presets first if required.

### 5. Release Layout

A software change creates a new Release. Additional Maya compatibility for unchanged software is added as another asset in the existing Release:

```text
Release: v1.0.0.0-beta
- UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2023_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2025_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2026_pyc.zip
```

For reproducible issues, submit a [GitHub Issue](https://github.com/SuirenkaZ/UntitleXTool/issues) with the Windows version, Maya version, package filename, steps, and screenshots without license or credential data.

---

## 中文

### 1. 支持的安装包

当前为 Windows 平台的 `v1.0.0.0-beta` 内测发布版本。由于不同 Maya 版本使用不同 Python 运行时与编译字节码，每个 Maya 版本均有独立安装包。

| Maya | Python 运行时 | 安装包 |
| --- | --- | --- |
| Maya 2022 | Python 3.7 | [下载 ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip) |
| Maya 2023 | Python 3.9 | [下载 ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2023_pyc.zip) |
| Maya 2024 | Python 3.10 | [下载 ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip) |
| Maya 2025 | Python 3.11 | [下载 ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2025_pyc.zip) |
| Maya 2026 | Python 3.11 | [下载 ZIP](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2026_pyc.zip) |

请勿将一个 Maya 版本的安装包安装到其他 Maya 版本中。

### 2. 文件校验

下载完成后，在 PowerShell 中运行：

```powershell
Get-FileHash -Algorithm SHA256 .\UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip
```

请按你的 Maya 版本替换文件名，并与以下结果比较：

| Maya | SHA-256 |
| --- | --- |
| Maya 2022 | `026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4` |
| Maya 2023 | `8DCDC49E01B959ABDF68FE53F00E9A741898C0AF25D1E8360689325AD78C0F5C` |
| Maya 2024 | `328537018E35B23C64CFA8191022511240D8CA304F0C3AE747EF5AB717DA16CF` |
| Maya 2025 | `70ABB43F6FAD6160E645B1D01CB30A02AF023C00DFF4C5D58C1166F259537BC3` |
| Maya 2026 | `48F5D395B9C8AEDAE20ADF1171A86863561A360A7F702C928DC656FCDEF4EFD0` |

校验值不一致的文件不要继续安装。

### 3. 安装步骤

1. 下载与你的 Maya 版本匹配的 ZIP，并完整解压到本地文件夹。
2. 确认解压目录中同时存在 `install.py` 与 `UntitleXTool` 文件夹。
3. 启动对应版本的 Autodesk Maya。
4. 将 `install.py` 拖入 Maya 主窗口或视图区域。
5. 确认安装器识别的 Maya 版本和用户 scripts 目录后，点击“安装 / 更新”。
6. 安装完成后，在 `UntitleTool` shelf 中打开 `UntitleXTool WorkBench`。

正确的解压结构如下：

```text
UntitleXTool_<version>_Maya<year>_pyc/
|-- install.py
|-- README.txt
`-- UntitleXTool/
    |-- load.pyc
    |-- main.pyc
    |-- uninstall.pyc
    `-- ...
```

`install.py` 与完整的 `UntitleXTool` 文件夹必须保持在同一层级，不要从压缩包预览窗口中直接运行。

### 4. License、更新与卸载

需要激活授权功能时，在 WorkBench 中打开 `设置 > 插件设置 > License`，输入购买后获得的 License Key 并点击“激活”。不要在公开截图或 Issue 中提供 License Key 与 `.lic` 文件。

更新时，请下载最新 Release 中与你的 Maya 版本一致的附件，解压后重新运行 `install.py`。安装器会在替换前备份已有工具目录。

卸载时，请使用 `UntitleTool` shelf 中的删除入口，完成后重启 Maya；如果存在需要保留的自定义预设，请提前备份。

### 5. 发布结构

软件内容发生变化时创建新的 Release；如果软件内容未变，只增加对某个 Maya 版本的支持，则将新附件添加到现有 Release：

```text
Release: v1.0.0.0-beta
- UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2023_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2025_pyc.zip
- UntitleXTool_1.0.0.0-beta_Maya2026_pyc.zip
```

如需反馈可复现的问题，请提交 [GitHub Issue](https://github.com/SuirenkaZ/UntitleXTool/issues)，并提供 Windows 版本、Maya 版本、安装包文件名、复现步骤及不含授权或凭证信息的截图。