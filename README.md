# MacRAR — 免费开源的 macOS RAR 解压工具（RAR Unarchiver for Mac）

MacRAR 是一款**免费、开源、原生 SwiftUI** 的 macOS 压缩与解压工具，用于在 Mac 上打开、预览和解压 **RAR、ZIP、7z、TAR 系列、分卷压缩包以及加密压缩包（含 AES-256 ZIP）**，也可用于创建压缩包。内置 RAR 7.30、UnRAR 与 7-Zip 26.04 三个命令行引擎，无第三方依赖、无遥测，所有文件处理均在本机完成；v1.3.1 及更早版本无任何网络请求，v1.3.2 起可选启用自动检查更新（每两天一次、闲时触发，仅访问 GitHub Releases，不提供手动检查）。

如果你正在找「Mac 怎么解压 RAR」「unrar for macOS」「The Unarchiver 替代品」，或一款离线、免费、可审查源码的 RAR extractor，MacRAR 是一个轻量选择。本仓库统一管理各版本的**更新历史**、**DMG 安装包下载**与**源码 / Xcode 工程包**。

## 功能特性

- **格式覆盖广**：RAR、ZIP、7z、TAR 系列（`tar.gz` / `tgz` / `tbz2` / `txz`）、分卷包，以及 `.iso`、`.cab`、`.lzh/.lha`、`.bz2`、`.xz`；支持归档完整性测试。
- **加密压缩包直接解压**：ZIP（ZipCrypto / AES-256，含中文文件名）、RAR（条目加密与 `-hp` 头部加密，含 RAR5）、7z（条目加密与 `-mhe=on` 头部加密）；密码只在本机内存中传给内置引擎，不写入磁盘或日志，命令日志以 `••••••` 脱敏。
- **Finder 右键集成**：右键即可压缩、解压、预览压缩包内容，支持嵌套压缩包预览，无需先展开整个包；加密包可在当前浮窗内直接输入密码。
- **原生 macOS 体验**：SwiftUI + AppKit 手写界面，菜单栏托盘、进度面板与 Finder 服务；内置 7 种界面语言（简体中文、繁体中文、English、日本語、한국어、Français、Русский），跟随系统语言切换。
- **隐私优先**：所有文件处理均在本机完成，无遥测、不上传任何文件；v1.3.1 及更早版本完全离线，v1.3.2 起可选启用自动检查更新（每两天一次、闲时触发，仅访问 GitHub Releases）。每个 Release 均附带完整源码与 Xcode 工程，可自行执行 `bash tools/build.sh` 构建。
- **开源免费**：以 [MIT License](LICENSE) 授权。

## 下载

所有版本的安装包（`.dmg`）都在 **[Releases](https://github.com/UltraPlusPro/MacRAR/releases)** 页面发布。

- 最新稳定版：**v1.3.3**（Latest）
- 最新预发布：**v1.3.2**（Pre-release）
- 其他预发布（测试用）：**v1.3.0**、**v1.2.6**（Pre-release）

## 安装

1. 进入 [Releases](https://github.com/UltraPlusPro/MacRAR/releases) 页面，下载所需版本（稳定版 `MacRAR 1.3.3.dmg`，或预发布 `MacRAR 1.3.2.dmg` / `MacRAR 1.3.0.dmg` / `MacRAR 1.2.6.dmg`）。
2. 双击挂载 DMG 镜像。
3. 将 `MacRAR.app` 拖入“应用程序”文件夹。
4. 从启动台打开即可使用。

> 安装包为 ad-hoc 签名、未公证。首次打开若提示「无法验证开发者」，可在「系统设置 → 隐私与安全性」点「仍要打开」，或右键 App →「打开」。1.3.0 及之后的版本也可在终端执行一次 `sudo xattr -dr com.apple.quarantine /Applications/MacRAR.app`。

## 更新历史

每个版本的变更说明与下载链接均在 [Releases](https://github.com/UltraPlusPro/MacRAR/releases) 页面的更新日志中记录，建议优先从那里获取最新版本。

## 系统要求

- macOS 11 (Big Sur) 或更高版本
- 支持 Apple Silicon 与 Intel 机型

> 注：上述系统要求为初始占位说明，请以实际安装包为准，可在 Releases 说明中补充修正。

## 开源协议

本项目以 [MIT License](LICENSE) 开源。
