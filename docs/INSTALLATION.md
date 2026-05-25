# UntitleXTool Installation, Activation, and Release Guide

## English

### 1. Status and Supported Environment

This is a beta/pre-release build intended for testing installation, licensing, and production workflows.

| Item | Current Support |
| --- | --- |
| Operating system | Windows |
| Available Maya package | Autodesk Maya 2022 |
| Installation method | Drag `install.py` into the Maya window |
| Current release | `v1.0.0.0-beta` |
| Maya 2022 asset | `UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip` |

Every Maya version must use its matching ZIP asset. A package compiled for Maya 2022 must not be installed into Maya 2023, 2024, or 2025.

### 2. Release and Maya Package Layout

One UntitleXTool software version is represented by one GitHub Release. That Release contains one asset for each supported Maya version:

```text
Release: v1.0.0.0-beta
- UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip   Available
- UntitleXTool_1.0.0.0-beta_Maya2023_pyc.zip   Added when available
- UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip   Added when available
- UntitleXTool_1.0.0.0-beta_Maya2025_pyc.zip   Added when available
```

When only Maya compatibility is added without changing the software version, an additional asset is added to the existing Release. When features, bug fixes, licensing behavior, or installation behavior changes, a new Release is created and new matching Maya assets are uploaded.

### 3. Download and Verify

Download the asset matching your Maya version from [GitHub Releases](https://github.com/SuirenkaZ/UntitleXTool/releases). The currently available package is:

- Maya 2022: [UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip)

Verify the Maya 2022 package in PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip
```

Expected value:

```text
026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4
```

If the value differs, delete the file and download it again before installation.

### 4. Extracted Package Structure

Extract the ZIP completely to a local folder before installation. The expected Maya 2022 structure is:

```text
UntitleXTool_1.0.0.0-beta_Maya2022_pyc/
|-- install.py
|-- README.txt
`-- UntitleXTool/
    |-- load.pyc
    |-- main.pyc
    |-- uninstall.pyc
    `-- ...
```

Keep `install.py` and the `UntitleXTool` folder at the same level. Do not drag a file directly out of an unopened ZIP preview.

### 5. Installation

1. Start the Maya version matching the downloaded package. For the current asset, start Autodesk Maya 2022.
2. Drag the extracted `install.py` into the Maya main window or viewport.
3. The installer detects the running Maya version and its user scripts location.
4. Confirm that the detected Maya version matches the ZIP asset, then click `Install / Update`.
5. After completion, open `UntitleXTool WorkBench` from the `UntitleTool` shelf.

When updating, the installer backs up the existing installed tool directory before replacing it.

### 6. License Activation

1. Open `UntitleXTool WorkBench`.
2. Go to `Settings > Plugin Settings > License`.
3. Enter the License Key received after purchase and click `Activate`.
4. Licensed features are available after activation succeeds.

License Keys and `.lic` files are personal license information. Never include them in public issues, logs, or screenshots.

### 7. Update and Uninstall

For an update, download the latest Release asset matching your Maya version, extract it, and run its `install.py` again. Do not select an asset for another Maya version.

To uninstall, use the removal action in the `UntitleTool` shelf and restart Maya after the uninstall finishes. Back up any custom presets you need to preserve before removal.

### 8. Troubleshooting and Issue Reports

If the installer does not open, confirm the ZIP was fully extracted and `install.py` remains beside the full `UntitleXTool` folder. If the shelf does not appear, restart Maya and verify that the installed scripts path belongs to the intended Maya version. If activation fails, check network access and enter the complete License Key again without sharing it publicly.

For issues, provide your Windows version, Maya version, package filename, reproducible steps, and screenshots without license or credential data in [GitHub Issues](https://github.com/SuirenkaZ/UntitleXTool/issues).

---

## 中文

### 1. 发布状态与适用环境

当前为内测版本，用于验证实际制作流程中的安装、授权与工具使用体验。

| 项目 | 当前支持范围 |
| --- | --- |
| 操作系统 | Windows |
| 已提供的 Maya 安装包 | Autodesk Maya 2022 |
| 安装方式 | 将 `install.py` 拖入 Maya 窗口 |
| 当前发布版本 | `v1.0.0.0-beta` |
| Maya 2022 附件 | `UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip` |

每个 Maya 版本必须使用其对应的 ZIP 附件。为 Maya 2022 编译的安装包不能安装到 Maya 2023、2024 或 2025 中混用。

### 2. 发布版本与 Maya 安装包结构

一个 UntitleXTool 软件版本对应一个 GitHub Release。同一个 Release 中，按支持的 Maya 版本分别放置安装包附件：

```text
Release: v1.0.0.0-beta
- UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip   已发布
- UntitleXTool_1.0.0.0-beta_Maya2023_pyc.zip   可用后添加
- UntitleXTool_1.0.0.0-beta_Maya2024_pyc.zip   可用后添加
- UntitleXTool_1.0.0.0-beta_Maya2025_pyc.zip   可用后添加
```

如果软件代码未变化，只新增 Maya 版本兼容包，则将对应附件加入已有 Release。如果功能、修复内容、授权逻辑或安装逻辑发生变化，则创建新的 Release，并上传新版本对应的 Maya 附件。

### 3. 下载与校验

请从 [GitHub Releases](https://github.com/SuirenkaZ/UntitleXTool/releases) 中选择与你的 Maya 版本一致的附件。当前已提供：

- Maya 2022：[UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip)

在 PowerShell 中校验 Maya 2022 安装包：

```powershell
Get-FileHash -Algorithm SHA256 .\UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip
```

校验结果应为：

```text
026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4
```

如果校验值不一致，请删除该文件并重新下载，不要继续安装。

### 4. 解压后的目录结构

安装前必须将 ZIP 完整解压到普通本地文件夹。Maya 2022 安装包的正确结构如下：

```text
UntitleXTool_1.0.0.0-beta_Maya2022_pyc/
|-- install.py
|-- README.txt
`-- UntitleXTool/
    |-- load.pyc
    |-- main.pyc
    |-- uninstall.pyc
    `-- ...
```

`install.py` 与 `UntitleXTool` 文件夹必须保持在同一层级。不要只复制 `install.py`，也不要直接从压缩包预览窗口拖拽运行。

### 5. 安装步骤

1. 启动与你下载的安装包对应的 Maya 版本；当前附件请启动 Autodesk Maya 2022。
2. 将解压后的 `install.py` 拖入 Maya 主窗口或视图区域。
3. 安装器会识别正在运行的 Maya 版本及对应的用户 scripts 路径。
4. 确认识别到的 Maya 版本与 ZIP 附件一致后，点击“安装 / 更新”。
5. 安装完成后，在 `UntitleTool` shelf 中打开 `UntitleXTool WorkBench`。

执行更新安装时，安装器会在覆盖前备份已安装的工具目录。

### 6. License 激活

1. 打开 `UntitleXTool WorkBench`。
2. 进入 `设置 > 插件设置 > License`。
3. 输入购买后获得的 License Key，并点击“激活”。
4. 激活成功后即可使用已授权功能。

License Key 与 `.lic` 文件属于个人授权资料。不要在公开 Issue、日志或截图中发送这些内容。

### 7. 更新与卸载

更新时，请下载最新 Release 中与你的 Maya 版本匹配的附件，完整解压后再次运行其中的 `install.py`。不要选择其他 Maya 版本的附件。

卸载时，请使用 `UntitleTool` shelf 中的删除入口，并在卸载完成后重启 Maya。若需要保留自定义配置或预设，请在卸载前进行备份。

### 8. 问题排查与反馈

如果拖拽后安装器没有出现，请确认 ZIP 已完整解压，并且 `install.py` 旁边仍有完整的 `UntitleXTool` 文件夹。如果找不到 shelf，请重启 Maya 并确认安装 scripts 路径属于目标 Maya 版本。如果 License 激活失败，请检查网络并重新输入完整 Key，不要公开发送 Key。

提交问题时，请在 [GitHub Issues](https://github.com/SuirenkaZ/UntitleXTool/issues) 中提供 Windows 版本、Maya 版本、安装包文件名、可复现步骤及不含授权或凭证信息的截图。