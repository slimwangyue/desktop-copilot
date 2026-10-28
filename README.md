# Desktop Copilot

Windows 桌面助手：看懂屏幕上的内容，帮你操作网页和桌面应用。模型在你自己的电脑上运行。

## 下载安装

到 [Releases](../../releases/latest) 下载最新的 `DesktopCopilot-vX.Y.Z-x64-setup.exe`，双击安装。

- 装在当前用户下，不需要管理员权限。
- 第一次打开时会检测显卡和内存，推荐合适的模型，然后自动下载并安装所需组件（Hermes、Strata、模型）。模型有十几到几十 GB，默认放在剩余空间最多的磁盘，可以修改。
- 如果要让它操作网页，安装过程中会提示你在 Chrome 里手动加载一个扩展（Chrome 只允许手动添加）。

### 系统要求

- Windows 10 / 11，64 位
- 建议 NVIDIA 显卡；内存和显存越大，可用的模型越好
- 首次安装需要能访问 GitHub 和模型下载站点

### 校验下载

每个安装包旁边都有 `.sha256` 文件，可以在 PowerShell 里核对：

```powershell
Get-FileHash .\DesktopCopilot-vX.Y.Z-x64-setup.exe -Algorithm SHA256
```

### Windows 提示"无法识别的应用"

安装包目前还没有代码签名，Windows SmartScreen 会提示风险。确认是从本页下载、校验值一致后，点"更多信息" → "仍要运行"。

## 卸载

在"设置 → 应用"里卸载 Desktop Copilot。Hermes、Strata 和已下载的模型体积较大，卸载时会保留，不需要的话可以手动删除（安装界面里显示过它们的位置）。

## 反馈

问题和建议请提 [Issue](../../issues)。

## 第三方组件

安装时从各项目的官方来源下载以下开源组件的固定版本，各自遵循其许可证；具体版本见每个 Release 的说明。

- [Hermes Agent](https://github.com/NousResearch/hermes-agent)（MIT）
- [Hermes Chrome plugin](https://github.com/waitkeeper/hermes-chrome-plugin)（MIT）
- [Strata](https://github.com/Niko1221/Strata)（MIT；模型有各自的许可证，安装时由 Strata 显示）
- [uv](https://github.com/astral-sh/uv)（MIT 或 Apache-2.0）

本仓库只用于发布安装包，不包含源代码。
