# UntitleXTool 安装、激活与使用说明

## 1. 发布状态与适用环境

本版本为内测版本，用于验证实际制作流程中的安装、授权与工具使用体验。

| 项目 | 支持范围 |
| --- | --- |
| 操作系统 | Windows |
| Maya 版本 | Autodesk Maya 2022 |
| 安装方式 | 拖拽 `install.py` 到 Maya 窗口 |
| 安装包名称 | `UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip` |

不同 Maya 版本使用各自对应的安装包。Maya 2022 安装包不要复制到 Maya 2023、2024 或 2025 环境中混用。

## 2. 下载安装包

从 [GitHub Releases](https://github.com/SuirenkaZ/UntitleXTool/releases) 下载 Maya 2022 ZIP 安装包。若使用备用链接，请在 [下载页面](http://62.234.16.253/#download) 切换到 `Maya 2022` 后按页面提示下载。

下载完成后，可用 PowerShell 检查文件完整性：

```powershell
Get-FileHash -Algorithm SHA256 .\UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip
```

校验结果应为：

```text
026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4
```

如校验值不一致，请删除该文件并重新下载，不要继续安装。

## 3. 解压后的目录结构

必须先将 ZIP 完整解压到普通本地文件夹。正确结构如下：

```text
UntitleXTool_1.0.0.0-beta_Maya2022_pyc/
├─ install.py
├─ README.txt
└─ UntitleXTool/
   ├─ load.pyc
   ├─ main.pyc
   ├─ uninstall.pyc
   └─ ...
```

`install.py` 和 `UntitleXTool` 文件夹必须保持在同一层级。请勿只复制 `install.py`，也不要在压缩包查看窗口中直接拖拽运行。

## 4. Maya 2022 安装步骤

1. 关闭正在执行批处理或正在保存场景的 Maya 操作。
2. 打开 Autodesk Maya 2022。
3. 从已解压的文件夹中，将 `install.py` 拖入 Maya 主窗口或视图区域。
4. 安装窗口会识别当前 Maya 版本及对应的用户 scripts 路径。
5. 确认识别结果为 Maya 2022 路径后，点击“安装 / 更新”。
6. 等待安装完成提示出现。
7. 切换到 Maya 的 `UntitleTool` shelf 标签，点击工具入口打开 `UntitleXTool WorkBench`。

安装器会将工具包复制到当前 Maya 用户 scripts 目录。重复安装新版本时，原有工具目录会在覆盖前被备份。

## 5. License 激活

授权功能需要 License Key：

1. 打开 `UntitleXTool WorkBench`。
2. 进入 `设置 > 插件设置`，切换到 `License` 页面。
3. 输入获得的 License Key，点击“激活”。
4. 页面显示激活成功后，即可使用已授权功能。

License Key 与本机授权信息属于个人授权资料。提交反馈时不要公开发送 Key、`.lic` 文件或包含授权内容的截图。

## 6. 更新安装

当 Maya 2022 新的内测包发布后：

1. 下载新的 Maya 2022 安装包并核对版本及 SHA-256。
2. 完整解压新安装包。
3. 再次将新包中的 `install.py` 拖入 Maya 2022。
4. 点击“安装 / 更新”，等待安装完成。
5. 重启 Maya 后使用新版本。

正常覆盖安装不会要求重新创建授权；若出现授权提示，请先确认网络与本机环境未改变，再反馈具体提示信息。

## 7. 卸载

1. 打开 Maya 的 `UntitleTool` shelf。
2. 点击删除入口并确认卸载。
3. 关闭并重新启动 Maya。

卸载前如有自定义项目配置或预设，请自行备份需要保留的内容。

## 8. 常见问题

### 拖拽 `install.py` 后没有出现安装窗口

- 确认使用的是 Maya 2022。
- 确认文件已经从 ZIP 中完整解压。
- 确认拖拽的是外层 `install.py`，且旁边仍有完整的 `UntitleXTool` 文件夹。

### 安装后找不到工具入口

- 在 Maya shelf 标签中查找 `UntitleTool`。
- 安装完成后重启 Maya，再次检查 shelf。
- 重新运行安装器，确认它识别的 scripts 目录属于 Maya 2022。

### License 无法激活

- 检查网络连接是否可访问授权服务。
- 确认 License Key 未缺字、多空格或粘贴错误。
- 记录界面上显示的错误提示后反馈，不要同时发送完整 Key。

### Windows 提示文件被阻止或安全警告

安装包包含 Maya 插件代码与辅助程序。请确认下载来源为本仓库 Releases 或官方公布的备用下载页，并先核对 SHA-256；来源或校验值不一致的文件不要运行。

## 9. 反馈问题时提供的信息

请在 [GitHub Issues](https://github.com/SuirenkaZ/UntitleXTool/issues) 中提供：

- Windows 与 Maya 的具体版本。
- 使用的安装包文件名。
- 可重复的操作步骤。
- 界面错误提示或不含敏感授权信息的截图。

请勿提交 License Key、`.lic` 文件、服务器凭证、私人项目素材或包含这些信息的日志。