<div align="center">

# 砚白 (Yanbai) Markdown 编辑器

**基于 Rust + Tauri 2.0 + React 19 构建的现代化所见即所得双语 Markdown 编辑器**

[![Release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?color=a85d3e&logo=github)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
[![Rust](https://img.shields.io/badge/Rust-1.85+-orange?logo=rust)](https://www.rust-lang.org/)
[![Tauri](https://img.shields.io/badge/Tauri-2.0-24C8D8?logo=tauri)](https://tauri.app/)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)](https://react.dev/)

[English](README.md) | **简体中文**

[功能特性](#核心特性) • [最新发布与下载](#下载与安装) • [架构设计](#架构设计) • [从源码构建](#从源码构建) • [版权说明](#版权说明)

</div>

---

## 简介

**砚白 (Yanbai)** 承袭温润陶土设计美学，专为追求专注排版与纯粹书写的创作者打造。

相较于传统基于 Electron 的沉重编辑器，砚白采用 **纯 Rust 核心引擎 + Tauri 2.0** 架构，体积小巧（独立安装包仅 13MB 左右）、极速冷启动、内存占用低，并具备零外部依赖的 Word 互转能力与单画布行内所见即所得体验。

---

## 核心特性

### 单画布行内所见即所得 (In-place WYSIWYG)
- **单画布沉浸创作** ：告别割裂的双栏左右分屏，提供类似 Typora 的居中独立纸张画布体验。
- **原地渲染与编辑流** ：公式、表格、代码块、图表、Callout 提示框原地渲染；点击任意内容即可原地进入编辑状态，失焦自动恢复富文本排版。
- **行内待办互动** ：任务列表 `- [ ]` 可以在渲染状态下直接点击打勾或取消，即时双向同步底层 Markdown 源码。

### 纯 Rust 打造的文档引擎 (`crates/yanbai-core`)
- **Word 97-2003 (.doc) 零依赖解析** ：纯 Rust OLE2 Compound File 二进制流解析，无需依赖微软 Office 或 LibreOffice，即可将旧版 `.doc` 快速解析为结构干净的 Markdown。
- **双向 Word 文档 (.docx) 转换** ：
  - 基于轻量级 XML 解析的 `.docx` 导入器，精准识别标题层级、粗斜体、列表、超链接与表格。
  - 基于标准 OOXML 的原生 `.docx` 逆向导出生成器，版式规整，自带标准中文排版样式。
- **智能多编码自动探测** ：内置 BOM 校验、严格 UTF-8 检测与 `chardetng` 编码探测（自动回退 GBK / Windows-936），配备 SHA-256 指纹去重，彻底消除中文乱码。
- **会话持久化与崩溃防护** ：后台自动防抖备份脏文档草稿，具备 64MB 恶意超大文件安全熔断机制。

### 强大的学术与可视化排版支持
- **KaTeX 矢量数学公式** ：毫秒级即时排版行内公式（如 `$E=mc^2$`）与复杂块级公式（如 `$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$`）。
- **Mermaid 结构图表** ：开箱支持流程图、时序图、甘特图、类图、状态图、思维导图等。
- **多彩 Callout 状态提示框** ：完整支持 GitHub 与 Obsidian 风格语法（`[!NOTE]`、`[!TIP]`、`[!IMPORTANT]`、`[!WARNING]`、`[!CAUTION]`）。
- **结构化表格支持** ：自动对齐排版，提供清爽雅致的数据呈现外观。

### 暖陶土设计美学与现代系统特性
- **温润陶土配色体系** ：选用护眼耐看的主题调色（主色 `#a85d3e`、提亮 `#e0a183`、象牙暖纸底色 `#fdfbf7`），支持深浅主题无缝切换。
- **Windows 11 Mica / Acrylic 材质** ：深度对接桌面窗口材质，通透典雅。
- **多标签页安全管理** ：
  - 支持多文档并行编辑、滚轮中键关标签、未保存修改圆点提醒。
  - **安全关闭拦截** ：关闭未保存标签页或退出程序时，智能弹出保存确认对话框，提供「保存 (S)」、「不保存 (D)」与「取消 (Esc)」选择，临时打字尝试不留任何多余文件。
  - 快捷键 `Ctrl+Shift+T` 随时恢复当前会话最近关闭的历史标签。
- **Windows 系统深度集成** ：
  - NSIS 安装程序内置可选注册 `.md` / `.markdown` 关联与资源管理器右键菜单「用砚白打开」。
  - 单实例（Single Instance）闭环：程序已运行时双击外部文档，自动置顶主窗口并在新标签页无缝打开。
  - 命令行冷/热启动传参开箱即用。
- **全格式导出** ：一键导出为 Word (`.docx`)、独立单文件离线 HTML（内嵌脚本离线可看）以及矢量 PDF 打印。
- **全局命令面板** ：按下 `Ctrl+K` 快速唤起命令中心，支持字母及模糊搜索所有功能。

---

## 下载与安装

前往 [GitHub Releases](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest) 获取各平台最新安装包：

| 平台 | 架构 | 文件名 | 说明 |
| :--- | :--- | :--- | :--- |
| **Windows** | x64 | `Yanbai-*-win64-installer.exe` | 推荐：NSIS 安装器（支持文件关联与右键菜单） |
| **Windows** | x64 | `Yanbai-*-win64.zip` | 绿色便携免安装版，解压即用 |
| **Windows** | ARM64 | `Yanbai-*-win-arm64-installer.exe` | Windows on ARM 的 NSIS 安装程序，原生 ARM64 构建 |
| **Windows** | ARM64 | `Yanbai-*-win-arm64.zip` | 适用于骁龙 / Surface Pro X 等 ARM64 设备 |
| **Linux** | x86_64 | `Yanbai-*-linux-x86_64.tar.gz` | Linux x86_64 预构建免安装压缩包 |
| **Linux** | ARM64 | `Yanbai-*-linux-arm64.tar.gz` | Linux aarch64 预构建免安装压缩包 |

---

## 架构设计

```
Yanbai/
├── crates/
│   └── yanbai-core/           # 纯 Rust 核心解析与数据引擎 (无 GUI 依赖，单元测试行覆盖 100%)
│       ├── src/
│       │   ├── doc97/         # Word 97-2003 (.doc) OLE2 二进制流解析与清洗
│       │   ├── docx/          # OOXML (.docx) 结构解析与逆向导出生成器
│       │   ├── encoding.rs    # 智能多编码探测 (UTF-8, GBK) 与 SHA-256 指纹检测
│       │   ├── recovery.rs    # 会话持久化与崩溃恢复序列化引擎
│       │   └── markdownescapes.rs # Markdown 转义与格式化工具
│       └── tests/             # 真实 .doc 与 .docx 样本与回归测试用例
├── src-tauri/                 # Tauri 2.0 桌面宿主与系统底层桥接
│   ├── src/
│   │   ├── lib.rs             # IPC 命令通道、单实例插件注册与系统事件编排
│   │   └── main.rs            # Windows/Linux/macOS 桌面应用入口
│   ├── capabilities/          # Tauri 2 权限声明 (dialog, fs, core)
│   └── tauri.conf.json        # 窗口效果 (Mica/Acrylic)、应用元数据与插件配置
├── frontend/                  # React 19 + Vite + Tailwind CSS v4 现代化前端
│   └── src/
│       ├── components/
│       │   ├── LiveEditor.tsx # 单画布所见即所得 (In-place WYSIWYG) 实时编辑器
│       │   ├── Editor.tsx     # 原生双栏源码编辑器
│       │   ├── Preview.tsx    # 独立富文本预览渲染容器
│       │   ├── TabBar.tsx     # 多标签页管理
│       │   ├── Toolbar.tsx    # 顶部格式化工具栏与视图切换器
│       │   ├── Outline.tsx    # 文档大纲 (TOC) 抽屉与平滑锚点定位
│       │   ├── StatusBar.tsx  # 状态统计栏 (中文字数、西文词数、编码、行列号)
│       │   ├── CommandPalette.tsx # 全局命令面板 (Ctrl+K)
│       │   └── SaveConfirmModal.tsx # 未保存文档关闭确认对话框 (保存/不保存/取消)
│       ├── utils/             # Markdown 解析、KaTeX 数学公式与 Mermaid 渲染引擎
│       └── App.tsx            # 全局标签状态、快捷键绑定与窗口事件中心调度器
└── tools/                     # 安装器与跨平台打包自动化脚本
```

---

## 从源码构建

### 前置依赖
- **Rust** 1.85+ (`rustc --version`)
- **Node.js** 20+ 与 **pnpm** 9+ (`pnpm --version`)
- Windows 10/11、Linux（安装 webkit2gtk-4.1 相关开发库）

### 1. 克隆代码仓库
```bash
git clone https://github.com/Speechlessmanbilibili/Yanbai.git
cd Yanbai
```

### 2. 运行核心库单元测试
```bash
cargo test --workspace
```

### 3. 安装前端依赖并启动开发环境
```bash
pnpm --prefix frontend install
pnpm --prefix frontend dev
```

### 4. 构建发布二进制
```bash
# 构建前端静态资源
pnpm --prefix frontend build

# 构建桌面端 Release 版本
cargo build --release --manifest-path src-tauri/Cargo.toml
```

产物将生成在 `target/release/` 目录下。

---

## 版权说明

本项目不是开源项目，源码不公开。[Yanbai-Releases](https://github.com/Speechlessmanbilibili/Yanbai-Releases) 上发布的安装包按[最终用户使用许可协议](LICENSE_zh.md)（英文版：[LICENSE.md](LICENSE.md)）授权：可以免费下载、安装，并在个人或商业环境中使用；不得再分发、售卖或发布修改版。

Copyright © 2026 SilentPerson. All rights reserved.
