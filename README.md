# UntitleXTool

## English

UntitleXTool is an Autodesk Maya asset production workbench for project, asset, and everyday production workflows inside Maya.

> Current status: **Beta / Pre-release**  
> Available package: **Windows + Autodesk Maya 2022**. Packages for additional Maya versions will be added as separate assets when available.

### Download

Each software version is published as one GitHub Release. Select the ZIP asset matching your Maya version from that release; packages built for different Maya versions must not be mixed.

| Maya Version | Current Package | Download |
| --- | --- | --- |
| Maya 2022 | `UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip` | [Download from GitHub Release](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip) |
| Maya 2023 | Not released | - |
| Maya 2024 | Not released | - |
| Maya 2025 | Not released | - |

Maya 2022 package verification:

```text
SHA-256  026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4
```

### Quick Installation

1. Download the ZIP matching your Maya version and fully extract it to a local folder.
2. Confirm that `install.py` and the `UntitleXTool` folder are at the same level.
3. Start the corresponding Autodesk Maya version. For the current package, use Maya 2022.
4. Drag `install.py` into the Maya main window or viewport.
5. Confirm the detected Maya scripts directory, then click `Install / Update` in the installer.
6. Open `UntitleXTool WorkBench` from the `UntitleTool` shelf after installation.

### License, Updates, and Support

Open `Settings > Plugin Settings > License` in WorkBench and enter the License Key received after purchase. Do not publish License Keys or `.lic` files in screenshots, issues, or logs.

For a software update, download the new Release asset matching your Maya version and run its installer again. A new compatible Maya package for the same software release will appear as an additional asset in that same Release.

Read the full [Installation, Activation, and Troubleshooting Guide](docs/INSTALLATION.md). For reproducible issues, submit a [GitHub Issue](https://github.com/SuirenkaZ/UntitleXTool/issues) with the Maya version, package filename, reproduction steps, and non-sensitive screenshots.

---

## 中文

UntitleXTool 是面向 Autodesk Maya 的资产生产工作台，用于在 Maya 内集中完成项目、资产及常用制作工具工作流。

> 当前状态：**内测版本 / Pre-release**  
> 已提供安装包：**Windows + Autodesk Maya 2022**。其他 Maya 版本会在可用时以独立附件形式加入对应发布版本。

### 下载

每一个软件版本对应一个 GitHub Release。同一个 Release 中按 Maya 版本分别提供 ZIP 安装包；用户只需下载与自己 Maya 版本一致的附件，不同 Maya 版本的安装包不能混用。

| Maya 版本 | 当前安装包 | 下载 |
| --- | --- | --- |
| Maya 2022 | `UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip` | [从 GitHub Release 下载](https://github.com/SuirenkaZ/UntitleXTool/releases/download/v1.0.0.0-beta/UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip) |
| Maya 2023 | 待发布 | - |
| Maya 2024 | 待发布 | - |
| Maya 2025 | 待发布 | - |

Maya 2022 安装包校验值：

```text
SHA-256  026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4
```

### 快速安装

1. 下载与你的 Maya 版本匹配的 ZIP 安装包，并完整解压到本地文件夹。
2. 确认解压目录的同一层级存在 `install.py` 与 `UntitleXTool` 文件夹。
3. 启动对应版本的 Autodesk Maya；当前安装包请使用 Maya 2022。
4. 将 `install.py` 拖入 Maya 主窗口或视图区域。
5. 在安装窗口中确认自动识别的 Maya scripts 目录，然后点击“安装 / 更新”。
6. 安装完成后，在 `UntitleTool` shelf 中打开 `UntitleXTool WorkBench`。

### License、更新与反馈

在 WorkBench 中打开 `设置 > 插件设置 > License`，填写购买后获得的 License Key 并完成激活。不要在截图、Issue 或日志中公开 License Key 与 `.lic` 文件。

软件版本更新时，请下载新 Release 中与你的 Maya 版本匹配的附件并重新运行安装器。同一软件版本新增 Maya 兼容包时，该附件会直接加入同一个 Release。

查看完整的[安装、激活与问题排查文档](docs/INSTALLATION.md)。遇到可复现的问题时，请提交 [GitHub Issue](https://github.com/SuirenkaZ/UntitleXTool/issues)，并提供 Maya 版本、安装包文件名、复现步骤与不含敏感授权信息的截图。