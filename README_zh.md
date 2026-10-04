<div align="center">

# 砚白 Markdown 编辑器

**基于 Rust、Tauri 2 与 React 19 构建、提供四种写作视图的双语 Markdown 编辑器**

[![Release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?color=a85d3e&logo=github)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Speechlessmanbilibili/Yanbai-Releases/total?color=a85d3e)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases)

[English](README.md) | **简体中文**

[核心特性](#核心特性) • [下载与安装](#下载与安装) • [系统要求](#系统要求) • [问题反馈](#问题反馈) • [版权说明](#版权说明)

</div>

---

## 简介

**砚白 (Yanbai)** 采用温润陶土配色与专注的正文排版，支持双栏对照、实时连续画布、Markdown 原文编辑和独立预览。Rust 文档引擎提供 Word 导入与导出，无需安装 Office 或 LibreOffice。

这个仓库是分发页，只放安装包、预编译压缩包和这份说明；源码不公开。

---

## 核心特性

### 四种写作视图

- **双栏、实时、原文、预览**：默认使用双栏，下次启动恢复上次选择的模式；切回双栏即回到默认。
- **实时连续画布**：居中呈现连续文稿，编辑提示收在页边；单击正文、格式文本、代码或公式字形，在对应原文位置编辑，点击外部后恢复排版。按住 Alt 单击链接可编辑链接文字。
- **内容原地编辑**：公式、表格、代码块、图表与 Callout 在文稿内呈现，可进入对应内容的编辑状态。
- **任务列表**：呈现待办内容与完成状态，可进入编辑修改 Markdown 勾选标记。
- **正文链接**：HTTP(S)、`mailto` 与 `tel` 交给系统关联应用，锚点在当前文档内定位；相对路径从当前文档目录打开受支持的文件，并复用已有标签。未保存的新文档需先保存，再打开相对文件链接。
- **内嵌图片保护**：四种视图均保护内嵌图片字节；在文字编辑区显示为受保护的图片对象，可整图复制或删除，避免误改编码内容。
- **粘贴与拖入图片**：PNG、JPEG、GIF、BMP、WebP 原图以短相对路径插入，保存时直接复制到文档所在目录。同名图片哈希一致时复用，内容不同时提供选择。原生保存窗口默认勾选“包含图片资源”；取消勾选后保存可读的图片占位符。

### 纯 Rust 打造的文档引擎
- **Word 97-2003 (.doc) 零依赖解析**：纯 Rust 读取 OLE2 复合文档，无需 Office 或 LibreOffice，把旧版 `.doc` 解析成结构干净的 Markdown。
- **双向 Word 文档 (.docx) 转换**：导入时识别标题层级、粗斜体、列表、超链接与表格；导出时生成标准 OOXML，自带规整的中文排版样式。
- **常见文本文件编辑与另存**：可打开并按原扩展名保存 Markdown、JSON、YAML、TOML、CSV、HTML、代码与配置文件；“另存为”也可导出 Word (`.docx`)。
- **保留编码与显式转换**：保存沿用探测到的编码与 BOM，也可选择“另存为 UTF-8…”主动转换。损坏的编码文本或原编码无法表示的字符会明确报错。保存及另存回当前文件前检查外部修改；另存为和 Word/HTML 导出时阻止覆盖其他已打开文档。
- **会话持久化与崩溃防护**：后台防抖备份草稿，用加密内容池复用相同正文与存盘基线，兼容旧版恢复文件。

### 学术与可视化排版
- **KaTeX 矢量公式**：行内公式（如 `$E=mc^2$`）与块级公式毫秒级排版。
- **Mermaid 结构图表**：流程图、时序图、甘特图、类图、状态图、思维导图开箱可用。
- **Callout 提示框**：完整支持 GitHub 与 Obsidian 语法（`[!NOTE]`、`[!TIP]`、`[!IMPORTANT]`、`[!WARNING]`、`[!CAUTION]`）。
- **结构化表格**：自动对齐排版，不用手工数竖线。

### 暖陶土设计美学与系统集成
- **中英文界面与设置**：默认跟随系统语言，也可选择中文或英文并保留选择；许可全文在设置的次级页面查看。
- **温润陶土配色**（主色 `#a85d3e`、提亮 `#e0a183`、象牙纸底 `#fdfbf7`），默认跟随系统深浅色。设置提供“跟随系统”“浅色”“深色”；手动选择在重启后保留，切回跟随系统时清除额外偏好。
- **Windows 11 Mica / Acrylic 材质**窗口效果。
- **多标签页管理**：未保存圆点提醒、中键关标签，关闭未保存标签或退出时弹出「保存 (S) / 不保存 (D) / 取消 (Esc)」，`Ctrl+Shift+T` 恢复本次会话关闭过的标签。
- **Windows 深度集成**：安装程序可选注册 `.md` / `.markdown` 关联与右键菜单「用砚白打开」，单实例运行，支持命令行传参打开文件。
- **图片嵌入导出**：Word (`.docx`) 与单文件离线 HTML 可嵌入本地或 `data:` 图片，支持 PNG、JPEG、GIF、BMP 与 WebP。网络图片需先保存到本地并从文档引用；SVG 或无法取得的图片会报错。HTML 内含完整公式与图表，无需运行渲染脚本；另支持 PDF 打印。
- **全局命令面板**：`Ctrl+K` 唤起，支持模糊搜索所有功能。

---

## 下载与安装

前往[最新版本](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)按平台取用：

| 平台 | 架构 | 文件名 | 说明 |
| :--- | :--- | :--- | :--- |
| **Windows** | x64 | `Yanbai-*-win64-installer.exe` | 推荐。NSIS 安装程序，可注册文件关联与右键菜单 |
| **Windows** | x64 | `Yanbai-*-win64.zip` | 便携包，解压即用 |
| **Windows** | ARM64 | `Yanbai-*-win-arm64-installer.exe` | Windows on ARM 的 NSIS 安装程序，原生 ARM64 构建 |
| **Windows** | ARM64 | `Yanbai-*-win-arm64.zip` | 便携包，解压即用 |
| **Linux** | x86_64 | `Yanbai-*-linux-x86_64.tar.gz` | 预编译压缩包 |
| **Linux** | ARM64 | `Yanbai-*-linux-arm64.tar.gz` | 预编译压缩包 |
| **macOS** | Apple 芯片 | `Yanbai-*-macos-arm64.dmg` | 应用安装镜像；无开发者证书签名与公证 |
| **macOS** | Apple 芯片 | `Yanbai-*-macos-arm64.app.tar.gz` | 应用压缩包，与同架构 `.dmg` 包含同一份 `Yanbai.app`，二选一即可 |
| **macOS** | Intel | `Yanbai-*-macos-x64.dmg` | 应用安装镜像；无开发者证书签名与公证 |
| **macOS** | Intel | `Yanbai-*-macos-x64.app.tar.gz` | 应用压缩包，与同架构 `.dmg` 包含同一份 `Yanbai.app`，二选一即可 |

**Windows**：运行安装程序，或解压便携包后直接启动 `Yanbai.exe`。

**Linux**：将 `<version>` 替换为版本号，`<arch>` 替换为 `x86_64` 或 `arm64`（`uname -m` 显示 `aarch64` 时选 `arm64`），使用已下载文件的名称：

将 `<version>` 替换为下载的版本号；以下命令按本机架构选择 x86_64 或 ARM64：

```bash
version='<version>'
case "$(uname -m)" in
  x86_64) arch=x86_64 ;;
  aarch64|arm64) arch=arm64 ;;
  *) printf '%s\n' 'Unsupported architecture' >&2; exit 1 ;;
esac
tar -xzf "Yanbai-${version}-linux-${arch}.tar.gz"
cd "Yanbai-${version}-linux-${arch}"
./run.sh
```

**macOS**：同架构的 `.dmg` 与 `.app.tar.gz` 包含同一份 `Yanbai.app`，任选一种下载即可。打开 `.dmg` 并将砚白拖入“应用程序”；或解压 `.app.tar.gz`，再将 `Yanbai.app` 放入“应用程序”。两种格式使用相同的 ad-hoc 签名，没有开发者证书签名与公证；若 macOS 阻止启动，请按 [Apple 关于打开未识别开发者应用的说明](https://support.apple.com/zh-cn/102445)处理。

---

## 系统要求

- **Windows** 10 或 11，x64 或 ARM64。
- **Linux** x86_64 或 aarch64，需要 GTK 3 与 `webkit2gtk-4.1` 运行库。
- **macOS** 11（Big Sur）或更新版本，Apple 芯片或 Intel；安装系统更新，使系统 WebKit 达到 Safari 16.4 或更新版本。最低配置尚无 Mac 实机验收记录。

---

## 首次启动与本地数据

首次启动先显示原生许可窗口，提供中英文全文与重点提示。选择“同意并继续”后，在应用数据目录原子保存 `license-acceptance.json`，记录双语许可正文的 SHA-256、软件版本、同意时间及显示语言，然后打开编辑器。相同许可不会因版本或界面语言变化再次询问；正文变化、记录缺失或损坏时重新确认。记录无法保存时，不会进入编辑器。

选择“不同意并退出”、关闭窗口或按 Esc，不保存拒绝结果，不创建编辑器的 WebView、偏好、日志、草稿或图片缓存；下次启动再次询问。拒绝新许可不会清除旧版已经保存的数据。操作系统自身的进程记录不由应用控制。

应用数据目录在 Windows 为 `%APPDATA%/com.speechlessmanbilibili.yanbai`，Linux 为 `$XDG_DATA_HOME/com.speechlessmanbilibili.yanbai`（缺省 `~/.local/share/com.speechlessmanbilibili.yanbai`），macOS 为 `~/Library/Application Support/com.speechlessmanbilibili.yanbai`。

- 恢复草稿：仅备份当前有未保存更改的标签页，包含正文、存盘基线、编码、文件与图片基础目录、光标及滚动位置等恢复状态。编辑后约三秒写入本地加密的 `recovery.enc`；没有未保存更改时、正常确认退出后会清除草稿。旧的 `recovery.json` 仍可迁移读取。读取、解密或密钥异常时保留原文件，并暂停覆盖与清理。
- 恢复密钥：`recovery.key` 与草稿放在同一目录，正常关闭后保留。Windows 使用当前用户的 DPAPI 保护密钥，Linux/macOS 的密钥依赖本地文件权限。加密不代替设备访问控制。编辑期间删除草稿不会关闭自动备份，之后可能重新生成；请勿在应用运行时删改密钥。
- 图片资源：粘贴、拖入及 Word 导入的图片原件暂存于 `image-resources`，按内容哈希复用；保存时按“包含图片资源”的选择放入文档同目录。资源缓存不会随关闭文档自动删除；退出应用后可自行清理，但尚未保存到文档目录的图片及恢复草稿可能仍引用它。
- 偏好与运行时缓存：语言、主题和视图偏好由 WebView 本地存储保存；WebView 另维护自身的配置与缓存。它们不在恢复草稿中，关闭文档不会清除。
- 日志：同意许可后才启用本地诊断日志，记录运行时/框架诊断，不主动记录文档正文；错误信息可能包含路径。默认每份约 40 KB 后轮转，保留当前日志和一份旧日志，不在正常退出时删除。Windows 日志位于 `%LOCALAPPDATA%/com.speechlessmanbilibili.yanbai/logs`，Linux 位于上述应用数据目录的 `logs`，macOS 位于 `~/Library/Logs/com.speechlessmanbilibili.yanbai`。

这些本地数据不会由软件上传。Markdown 中的外链图片地址会保留，但当前应用的内容安全策略阻止正文直接加载外部图片，保存不会自动下载外链图片。主动打开外部链接可能交给浏览器并产生网络访问；独立 HTML 导出也限制外部资源加载。清理本地文件前请先正常退出并备份需要的文档和图片。

## 问题反馈

用着有问题或者想要新功能，到 [Issues](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues) 提。写清触发步骤，能给一个最小复现样例最好。Issue 公开可见，建议另造最小样例或先脱敏；反馈授权和保密等约定见使用许可第五节。

---

## 版权说明

官方产物按[砚白软件使用许可](LICENSE_zh.md)（英文版：[LICENSE.md](LICENSE.md)）授权：免费用于个人与商业目的，允许备份及向代表组织开展内部工作的关联方、员工和承包商部署。对外再分发、售卖、出租、公开软件仓库收录及打包分发须事先取得许可方的书面同意；已允许的内部部署不受此限。源码不公开，本许可不授予源码访问权。 随软件分发的第三方组件及其许可条款见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

Copyright © 2026 SilentPerson. All rights reserved.

