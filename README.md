# UntitleXTool

面向 Autodesk Maya 的资产生产工作台，用于在 Maya 内集中完成项目、资产及常用制作工具工作流。

> 当前发布状态：**内测版本**  
> 首个公开安装包面向 **Windows + Autodesk Maya 2022**。其他 Maya 版本的安装包尚未发布，请勿混用。

## 下载

- Maya 2022 安装包：请前往 [GitHub Releases](https://github.com/SuirenkaZ/UntitleXTool/releases) 下载 `UntitleXTool_1.0.0.0-beta_Maya2022_pyc.zip`。
- 百度网盘备用下载：访问 [UntitleXTool 下载页面](http://62.234.16.253/#download)，选择 `Maya 2022` 查看下载链接与提取码。

发布包校验值：

```text
SHA-256  026044F714869816AFD83650CD63B7606CEB6C3B7521C27B152BA0965A7E42F4
```

## 快速安装

1. 下载 ZIP 安装包并完整解压，不能直接从压缩包预览中运行安装文件。
2. 确认解压后的同一层级存在 `install.py` 与 `UntitleXTool` 文件夹。
3. 启动 Maya 2022，将 `install.py` 拖入 Maya 主窗口或视图区域。
4. 在安装窗口中确认自动识别的 Maya scripts 目录，点击“安装 / 更新”。
5. 安装完成后，在 Maya 的 `UntitleTool` shelf 中打开 `UntitleXTool WorkBench`。

## License 激活

首次使用授权功能时，在 WorkBench 中打开 `设置 > 插件设置 > License`，填写购买后获得的 License Key 并完成激活。License Key 仅供本人使用，不要在截图、问题反馈或公开文件中提供。

## 更新与卸载

- 更新：下载新的对应 Maya 版本安装包，重新拖拽 `install.py` 安装。安装器覆盖前会备份已安装目录。
- 卸载：在 `UntitleTool` shelf 中使用删除入口，完成后重启 Maya。

## 完整说明

查看 [安装、激活与问题排查文档](docs/INSTALLATION.md)，其中包含安装目录说明、校验方法、更新流程与常见故障处理。

## 反馈

遇到可复现的问题时，请在仓库中提交 Issue，并提供 Maya 版本、复现步骤与界面提示。不要上传 License Key、授权文件或包含个人路径和凭证的日志。