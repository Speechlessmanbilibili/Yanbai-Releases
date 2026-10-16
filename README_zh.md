<div align="center">

<img src="https://raw.githubusercontent.com/Speechlessmanbilibili/Yanbai-Releases/main/assets/readme/icon.png" width="80" height="80" alt="砚白应用图标">

# 砚白 · Yanbai

### 把精力留给内容。

一款温润、专注的 Markdown 文稿工作台。<br>连续实时编辑，清晰呈现公式与图表，自在往返 Markdown 与 Word。

[![最新版本](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?style=flat-square&color=a85d3e&label=Release)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
![支持的平台](https://img.shields.io/badge/Windows%20%C2%B7%20Linux%20%C2%B7%20macOS-a85d3e?style=flat-square)
[![下载次数](https://img.shields.io/github/downloads/Speechlessmanbilibili/Yanbai-Releases/total?style=flat-square&color=a85d3e)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases)

**[下载砚白](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)** · [了解功能](#为写作留出空间) · [安装指引](#下载与安装) · [反馈与建议](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues)

[English](README.md) | **简体中文**

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Speechlessmanbilibili/Yanbai-Releases/main/assets/readme/workspace-dark.png">
  <img src="https://raw.githubusercontent.com/Speechlessmanbilibili/Yanbai-Releases/main/assets/readme/workspace-light.png" alt="砚白实时模式：连续正文、行内公式、任务列表与表格，采用温润陶土配色和圆角画布" width="1200">
</picture>

<sub>实时模式的实际界面 · 随阅读主题切换深浅配图 · Windows 截图</sub>

</div>

---

## 为写作留出空间

| 连贯地写 | 清晰地表达 | 从容地交付 |
| :--- | :--- | :--- |
| 在连续页面里直接编辑，Markdown 符号随光标展开。 | 把公式、图表、表格与代码放回文稿之中。 | 接续 Word 材料，导出 `.docx`、独立 HTML，或打印为 PDF。 |

### 让思路连贯，让格式自然

粗体、斜体、高亮和行内代码在输入时保留样式；光标进入对应范围时显示 Markdown 符号，离开后隐藏。跨段选择、查找替换、撤销与重做都在同一份文稿中完成，切换标签或编辑视图后延续各文档的撤销历史。

| 写作视图 | 适合此刻的工作 |
| :--- | :--- |
| **实时** | 在连续排版的正文里直接写作与修改。 |
| **原文** | 专注 Markdown 文本与语法。 |
| **双栏** | 一边编辑原文，一边对照预览。 |
| **预览** | 阅读完整排版后的文稿。 |

默认使用双栏，下次启动记住你的选择。工具栏、右键菜单、快捷键、命令面板和行首 `/` 插入提供一致的编辑能力；没有选中文字时，同样可以从光标位置开始操作。

### 复杂的内容，也能清晰可读

- **公式与图表**：KaTeX 排版行内和块级公式，Mermaid 支持流程图、时序图、甘特图、思维导图等；编辑时源码与预览并存。
- **直接在表格里工作**：修改单元格，插入、删除、移动和对齐行列；按需复制为 Markdown、纯文本、CSV 或 HTML。
- **文稿需要的细节**：代码着色与复制、任务列表、Callout 提示框、脚注、引用式链接、文档属性和折叠内容。
- **图片跟着文稿走**：粘贴或拖入 PNG、JPEG、GIF、BMP、WebP，保存时将原图放在文档同目录，以相对路径引用；相同内容直接复用，文件冲突时提供选择。

### 从已有材料，写到正式交付

| 从这里开始 | 在砚白里继续 | 带走你的成果 |
| :--- | :--- | :--- |
| Markdown 与常见文本文件 | 保留原编码与 BOM，需要时通过“另存为 UTF-8…”明确转换。 | 按原扩展名保存文本。 |
| Word `.doc` 与 `.docx` | 由 Rust 文档引擎导入标题、格式、列表、链接、表格与图片。 | 无需安装 Office 或 LibreOffice，即可导出 `.docx`。 |
| 公式、图表与本地图片 | 在同一个工作台中整理文稿。 | 导出内含完整公式、图表及受支持图片的独立 HTML，或打印为 PDF。 |

按习惯调整字号和行宽，让深浅主题跟随系统，在中文与英文界面间自由切换。标签、大纲、查找与圆角画布让工作区保持有序；设置中也提供减少动态效果的选项。

保存前检查外部修改，避免覆盖其他已打开文档；本地加密恢复草稿保留尚未保存的工作，供中断后恢复。

## 下载与安装

前往[最新版本](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)，按系统与架构选择文件。文件名中的 `*` 表示版本号，例如 `2.5.0`。

Windows 的 Intel/AMD 设备通常选 x64，Windows on ARM 设备选 ARM64；macOS 按 Apple 芯片或 Intel 选择。

| 平台 | 架构 | 文件 | 用途 |
| :--- | :--- | :--- | :--- |
| **Windows** | x64 | `Yanbai-*-win64-installer.exe` | 安装器，可设置文件关联 |
| **Windows** | x64 | `Yanbai-*-win64.zip` | 便携包，解压即用 |
| **Windows** | ARM64 | `Yanbai-*-win-arm64-installer.exe` | 原生 ARM64 安装器 |
| **Windows** | ARM64 | `Yanbai-*-win-arm64.zip` | 原生 ARM64 便携包 |
| **Linux** | x86_64 | `Yanbai-*-linux-x86_64.tar.gz` | 预编译压缩包 |
| **Linux** | ARM64 | `Yanbai-*-linux-arm64.tar.gz` | 预编译压缩包 |
| **macOS** | Apple 芯片 | `Yanbai-*-macos-arm64.dmg` | 拖入“应用程序” |
| **macOS** | Apple 芯片 | `Yanbai-*-macos-arm64.app.tar.gz` | 同一应用的压缩包 |
| **macOS** | Intel | `Yanbai-*-macos-x64.dmg` | 拖入“应用程序” |
| **macOS** | Intel | `Yanbai-*-macos-x64.app.tar.gz` | 同一应用的压缩包 |

### Windows

运行安装器，或解压便携包并打开 `Yanbai.exe`。安装器可选设置 `.md` / `.markdown` 文件关联及“用砚白打开”右键菜单。

### Linux

先下载适合本机架构的压缩包，在下载目录打开终端。只需把 `version='<version>'` 中的 `<version>` 改为下载版本号（例如 `2.5.0`，不带 `v`）；以下命令通过 `uname -m` 自动识别架构，无需手动填写 `arch`。

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

### macOS

同架构的 `.dmg` 与 `.app.tar.gz` 包含同一份 `Yanbai.app`，任选一种即可。打开 `.dmg` 后将砚白拖入“应用程序”；或解压 `.app.tar.gz`，再将 `Yanbai.app` 移入“应用程序”。

两种格式均采用 ad-hoc 签名，未使用开发者证书签名或公证。若系统阻止启动，请参阅 [Apple 的打开说明](https://support.apple.com/zh-cn/102445)。

### 系统要求

- **Windows** 10 或 11，x64 或 ARM64。
- **Linux** x86_64 或 aarch64，需要 GTK 3 与 `webkit2gtk-4.1` 运行库。
- **macOS** 11（Big Sur）或更新版本，Apple 芯片或 Intel；安装系统更新，使系统 WebKit 达到 Safari 16.4 或更新版本。

## 几个顺手的操作

| 想做什么 | 操作 |
| :--- | :--- |
| 查找功能 | `Ctrl+K` 打开命令面板。 |
| 插入内容 | 在行首输入 `/`，或使用右键菜单。 |
| 打开正文链接 | 实时模式用 `Ctrl/Cmd + 单击`、中键或 `Ctrl/Cmd + Enter`；预览模式直接单击。 |
| 编辑表格 | 单击单元格进入，`Tab` / `Shift+Tab` 换格，`Enter` / `Esc` 结束。 |
| 重新打开标签 | `Ctrl+Shift+T` 恢复当前会话最近关闭的标签。 |

正文锚点在当前文档内定位，相对文件链接以文档所在目录为准；新建草稿先保存，再打开相对链接。外部链接交给系统关联应用。

## 文稿与本地数据

文档在本地处理，字体、公式与图表资源随应用提供。首次启动确认使用许可，同意记录保存后进入编辑器；相同许可无需因软件升级或切换语言再次确认。

原生保存窗口默认勾选“包含图片资源”；取消勾选时保存带可读图片占位符的副本，并保留完整编辑稿。Word 与 HTML 导出支持嵌入受支持的本地或 `data:` 图片。

<details>
<summary>展开：首次启动、草稿、图片、密钥与日志</summary>

首次启动先显示原生许可窗口，提供中英文全文与重点提示。选择“同意并继续”后，在应用数据目录原子保存 `license-acceptance.json`，记录双语许可正文的 SHA-256、软件版本、同意时间及显示语言，然后打开编辑器。相同许可不会因版本或界面语言变化再次询问；正文变化、记录缺失或损坏时重新确认。记录无法保存时，不会进入编辑器。

选择“不同意并退出”、关闭窗口或按 Esc，不保存拒绝结果，不创建编辑器的 WebView、偏好、日志、草稿或图片缓存；下次启动再次询问。拒绝新许可不会清除旧版已经保存的数据。操作系统自身的进程记录不由应用控制。

应用数据目录在 Windows 为 `%APPDATA%/com.speechlessmanbilibili.yanbai`，Linux 为 `$XDG_DATA_HOME/com.speechlessmanbilibili.yanbai`（缺省 `~/.local/share/com.speechlessmanbilibili.yanbai`），macOS 为 `~/Library/Application Support/com.speechlessmanbilibili.yanbai`。

- 恢复草稿：仅备份当前有未保存更改的标签页，包含正文、存盘基线、编码、文件与图片基础目录、光标及滚动位置等恢复状态。编辑后约三秒写入本地加密的 `recovery.enc`；没有未保存更改时、正常确认退出后会清除草稿。旧的 `recovery.json` 仍可迁移读取。读取、解密或密钥异常时保留原文件，并暂停覆盖与清理。
- 恢复密钥：`recovery.key` 与草稿放在同一目录，正常关闭后保留。Windows 使用当前用户的 DPAPI 保护密钥，Linux/macOS 的密钥依赖本地文件权限。加密不代替设备访问控制。编辑期间删除草稿不会关闭自动备份，之后可能重新生成；请勿在应用运行时删改密钥。
- 图片资源：粘贴、拖入及 Word 导入的图片原件暂存于 `image-resources`，按内容哈希复用；保存时按“包含图片资源”的选择放入文档同目录。资源缓存不会随关闭文档自动删除；退出应用后可自行清理，但尚未保存到文档目录的图片及恢复草稿可能仍引用它。
- 偏好与运行时缓存：语言、主题和视图偏好由 WebView 本地存储保存；WebView 另维护自身的配置与缓存。它们不在恢复草稿中，关闭文档不会清除。
- 日志：同意许可后才启用本地诊断日志，记录运行时/框架诊断，不主动记录文档正文；错误信息可能包含路径。默认每份约 40 KB 后轮转，保留当前日志和一份旧日志，不在正常退出时删除。Windows 日志位于 `%LOCALAPPDATA%/com.speechlessmanbilibili.yanbai/logs`，Linux 位于上述应用数据目录的 `logs`，macOS 位于 `~/Library/Logs/com.speechlessmanbilibili.yanbai`。

这些本地数据不会由软件上传。Markdown 中的外链图片地址会保留，但当前应用的内容安全策略阻止正文直接加载外部图片，保存不会自动下载外链图片。主动打开外部链接可能交给浏览器并产生网络访问；独立 HTML 导出也限制外部资源加载。清理本地文件前请先正常退出并备份需要的文档和图片。

</details>

## 反馈与建议

遇到问题，或有想要的功能？欢迎前往 [Issues](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues)。请写清操作步骤、系统和版本，必要时附上最小复现样例。Issue 公开可见，建议使用另造的样例或先脱敏；反馈授权与保密约定见使用许可第五节。

## 使用许可

官方产物按[砚白软件使用许可](LICENSE_zh.md)（[英文版](LICENSE.md)）授权。免费用于个人与商业目的，允许备份，以及向代表组织开展内部工作的关联方、员工和承包商部署。对外再分发、售卖、出租、公开软件仓库收录及打包分发，须事先取得许可方的书面同意；已允许的内部部署不受此限。源码不公开，本许可不授予源码访问权。

第三方组件及其许可见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。

---

<div align="center">

写下想法，留下作品。

<sub>Copyright © 2026 SilentPerson. All rights reserved.</sub>

</div>
