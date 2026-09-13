<div align="center">

# 砚白 Markdown 编辑器

**基于 Rust、Tauri 2.0 与 React 19 构建的现代单画布双语 Markdown 编辑器**

[![Release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?color=a85d3e&logo=github)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Speechlessmanbilibili/Yanbai-Releases/total?color=a85d3e)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases)

[English](README.md) | **简体中文**

[核心特性](#核心特性) • [下载与安装](#下载与安装) • [系统要求](#系统要求) • [问题反馈](#问题反馈) • [版权说明](#版权说明)

</div>

---

## 简介

**砚白 (Yanbai)** 承袭温润陶土设计美学，专为追求专注排版与纯粹书写的创作者打造。它采用纯 Rust 文档引擎加 Tauri 2.0 构建：独立安装包约 13 MB，冷启动快、内存占用低，Word 双向互转不需要装 Office 或 LibreOffice。

这个仓库是分发页，只放安装包、预编译压缩包和这份说明；源码不公开。

---

## 核心特性

### 单画布行内所见即所得 (In-place WYSIWYG)
- **单画布沉浸创作**：不分左右双栏，居中一张纸写到底。
- **原地渲染与编辑**：公式、表格、代码块、图表与 Callout 原地渲染，点一下就进编辑态，失焦自动回到排版结果。
- **行内待办互动**：渲染状态下的 `- [ ]` 可以直接点选，勾选结果即时写回 Markdown 源码。

### 纯 Rust 打造的文档引擎
- **Word 97-2003 (.doc) 零依赖解析**：纯 Rust 读取 OLE2 复合文档，无需 Office 或 LibreOffice，把旧版 `.doc` 解析成结构干净的 Markdown。
- **双向 Word 文档 (.docx) 转换**：导入时识别标题层级、粗斜体、列表、超链接与表格；导出时生成标准 OOXML，自带规整的中文排版样式。
- **智能多编码探测**：BOM 校验、严格 UTF-8 检测与 `chardetng` 探测（回退 GBK / Windows-936），配合 SHA-256 指纹，保存时沿原编码写回，不产生乱码。
- **会话持久化与崩溃防护**：后台防抖备份草稿，并有 64 MB 超大文件熔断。

### 学术与可视化排版
- **KaTeX 矢量公式**：行内公式（如 `$E=mc^2$`）与块级公式毫秒级排版。
- **Mermaid 结构图表**：流程图、时序图、甘特图、类图、状态图、思维导图开箱可用。
- **Callout 提示框**：完整支持 GitHub 与 Obsidian 语法（`[!NOTE]`、`[!TIP]`、`[!IMPORTANT]`、`[!WARNING]`、`[!CAUTION]`）。
- **结构化表格**：自动对齐排版，不用手工数竖线。

### 暖陶土设计美学与系统集成
- **温润陶土配色**（主色 `#a85d3e`、提亮 `#e0a183`、象牙纸底 `#fdfbf7`），深浅主题随时切换。
- **Windows 11 Mica / Acrylic 材质**窗口效果。
- **多标签页管理**：未保存圆点提醒、中键关标签，关闭未保存标签或退出时弹出「保存 (S) / 不保存 (D) / 取消 (Esc)」，`Ctrl+Shift+T` 恢复本次会话关闭过的标签。
- **Windows 深度集成**：安装程序可选注册 `.md` / `.markdown` 关联与右键菜单「用砚白打开」，单实例运行，支持命令行传参打开文件。
- **全格式导出**：Word (`.docx`)、单文件离线 HTML、矢量 PDF 打印。
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
| **macOS** | Apple 芯片 | `Yanbai-*-macos-arm64.dmg` | 未签名，首次打开要右键「打开」 |
| **macOS** | Intel | `Yanbai-*-macos-x64.dmg` | 未签名，首次打开要右键「打开」 |

**Windows**：运行安装程序，或解压便携包后直接启动 `Yanbai.exe`。

**Linux**：

```bash
tar -xzf Yanbai-<版本号>-linux-x86_64.tar.gz
cd Yanbai-<版本号>-linux-x86_64
./run.sh
```

**macOS**：打开 dmg，把「砚白」拖进「应用程序」。产物没有签名与公证，第一次打开会被 Gatekeeper 拦住，右键点图标选「打开」即可；也可以在终端执行：

```bash
xattr -dr com.apple.quarantine /Applications/Yanbai.app
```

不想用 dmg 的可以直接解压 `Yanbai-<版本号>-macos-<架构>.app.tar.gz`，里面就是 `.app`。

---

## 系统要求

- **Windows** 10 或 11，x64 或 ARM64。
- **Linux** x86_64 或 aarch64，需要 GTK 3 与 `webkit2gtk-4.1` 运行库。
- **macOS** 10.13 或更高，Apple 芯片或 Intel。

---

## 问题反馈

用着有问题或者想要新功能，到 [Issues](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues) 提。写清触发步骤，能给一个最小复现样例最好。不要附含机密信息或个人信息的内容：Issue 是公开的，协议也把反馈按非保密信息处理。提交 Issue 即表示你同意[贡献指南](CONTRIBUTING.md)里的反馈许可条款。

---

## 版权说明

本仓库分发的安装包按[最终用户使用许可协议](LICENSE_zh.md)（英文版：[LICENSE.md](LICENSE.md)）授权：可以免费下载、安装，并在个人或商业环境中使用；不得再分发、售卖或发布修改版。源码不公开，本许可不授予源码访问权。随软件分发的第三方组件及其许可条款见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。安装程序开始复制文件前会显示这份协议；装好之后，点工具栏右侧的「关于」按钮或用 `Ctrl+K` 命令面板也能随时查看全文。

Copyright © 2026 SilentPerson. All rights reserved.
