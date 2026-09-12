<div align="center">

# Yanbai Markdown Editor

**A modern, in-place WYSIWYG bilingual Markdown editor built with Rust, Tauri 2.0, and React 19**

[![Release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?color=a85d3e&logo=github)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
[![Rust](https://img.shields.io/badge/Rust-1.85+-orange?logo=rust)](https://www.rust-lang.org/)
[![Tauri](https://img.shields.io/badge/Tauri-2.0-24C8D8?logo=tauri)](https://tauri.app/)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)](https://react.dev/)

**English** | [简体中文](README_zh.md)

[Features](#key-features) • [Downloads & Releases](#download--installation) • [Architecture](#architecture) • [Building from Source](#building-from-source) • [Copyright & License](#copyright--license)

</div>

---

## Introduction

**Yanbai** (砚白) inherits a warm terracotta aesthetic, crafted specifically for writers and creators who value focused typography and pure writing flow.

Unlike bulky Electron-based editors, Yanbai is built on a **pure Rust core engine and Tauri 2.0** architecture. It delivers a compact footprint (standalone installer ~13 MB), instantaneous cold start, minimal memory consumption, zero-dependency bidirectional Word interoperability, and an in-place WYSIWYG single-canvas editing experience.

---

## Key Features

### In-place Single-Canvas WYSIWYG
- **Immersive Single-Canvas Writing** : Eliminates split-pane distractions, providing a centered, clean sheet-of-paper experience akin to Typora.
- **In-place Render and Edit Flow** : Formulas, tables, code blocks, diagrams, and callouts render in place. Click any element to edit directly; unfocusing instantly restores rich typography rendering.
- **Interactive Task Lists** : Click checkboxes `- [ ]` directly within the rendered view to toggle tasks, seamlessly synchronizing state with the underlying Markdown source.

### Document Engine Built in Pure Rust (`crates/yanbai-core`)
- **Zero-Dependency Word 97-2003 (.doc) Parsing** : Pure Rust OLE2 Compound File binary stream extraction without requiring Microsoft Office or LibreOffice, parsing legacy `.doc` files into clean Markdown structures.
- **Bidirectional Word (.docx) Conversion** :
  - Lightweight XML parser for `.docx` import, accurately recognizing headings, formatting, lists, hyperlinks, and tables.
  - Native standard OOXML generator for `.docx` export, producing clean typography with standard Chinese and Western typographic styling.
- **Intelligent Multi-Encoding Detection** : Built-in BOM verification, strict UTF-8 validation, and `chardetng` encoding detection (with automatic GBK / Windows-936 fallback) paired with SHA-256 fingerprinting to eliminate garbled text.
- **Session Persistence and Crash Recovery** : Background debounced dirty-draft autosave with a 64 MB malicious file safety fuse.

### Academic and Visual Typography
- **KaTeX Vector Mathematics** : Millisecond-level rendering for inline math (such as `$E=mc^2$`) and display math blocks (such as `$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$`).
- **Mermaid Diagrams** : Out-of-the-box support for flowcharts, sequence diagrams, Gantt charts, class diagrams, state diagrams, and mindmaps.
- **Callout Alert Blocks** : Full syntax support for GitHub and Obsidian callouts (`[!NOTE]`, `[!TIP]`, `[!IMPORTANT]`, `[!WARNING]`, `[!CAUTION]`).
- **Structured Tables** : Automatic alignment and formatting with an elegant, clear presentation.

### Warm Terracotta Aesthetic and Modern Desktop Integration
- **Warm Terracotta Palette** : Thoughtfully tuned eye-friendly tones (primary `#a85d3e`, highlight `#e0a183`, ivory paper background `#fdfbf7`), supporting seamless light and dark mode switching.
- **Windows 11 Mica and Acrylic Materials** : Deep integration with modern desktop window materials for a translucent, refined look.
- **Safe Multi-Tab Management** :
  - Concurrent multi-document editing, middle-click tab closure, and unsaved changes indicator dots.
  - **Safe Exit Guard** : Closing unsaved tabs or quitting the application triggers a confirmation modal offering "Save (S)", "Don't Save (D)", and "Cancel (Esc)", keeping casual typing experiments clean.
  - Hotkey `Ctrl+Shift+T` to restore recently closed tabs in the current session.
- **Deep Windows Integration** :
  - Optional `.md` / `.markdown` file association and explorer context menu "Open with Yanbai" via the NSIS installer.
  - Single-instance handling: opening files while running brings the main window forward and opens the document in a new tab.
  - Direct cold-start and warm-start command-line file argument support.
- **Comprehensive Export Options** : One-click export to Word (`.docx`), standalone offline HTML (embedded scripts and styles), and vector PDF printing.
- **Global Command Palette** : Press `Ctrl+K` to open the command palette with fuzzy search across all actions.

---

## Download & Installation

Visit [GitHub Releases](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest) to download the latest builds for your platform:

| Platform | Architecture | File Name | Description |
| :--- | :--- | :--- | :--- |
| **Windows** | x64 | `Yanbai-*-win64-installer.exe` | Recommended: NSIS installer (file associations and context menu) |
| **Windows** | x64 | `Yanbai-*-win64.zip` | Portable standalone package, extract and run |
| **Windows** | ARM64 | `Yanbai-*-win-arm64-installer.exe` | NSIS installer for Windows on ARM, native ARM64 build |
| **Windows** | ARM64 | `Yanbai-*-win-arm64.zip` | Portable standalone package, extract and run |
| **Linux** | x86_64 | `Yanbai-*-linux-x86_64.tar.gz` | Linux x86_64 prebuilt archive |
| **Linux** | ARM64 | `Yanbai-*-linux-arm64.tar.gz` | Linux aarch64 prebuilt archive |

---

## Architecture

```
Yanbai/
├── crates/
│   └── yanbai-core/           # Pure Rust document engine (no GUI dependencies, 100% line coverage)
│       ├── src/
│       │   ├── doc97/         # Word 97-2003 (.doc) OLE2 stream parser & sanitizer
│       │   ├── docx/          # OOXML (.docx) parser & reverse exporter
│       │   ├── encoding.rs    # Multi-encoding detector (UTF-8, GBK) & SHA-256 fingerprinting
│       │   ├── recovery.rs    # Session persistence & crash recovery serialization
│       │   └── markdownescapes.rs # Markdown escaping & sanitization utilities
│       └── tests/             # Real .doc and .docx sample regression tests
├── src-tauri/                 # Tauri 2.0 desktop shell & native OS bridging
│   ├── src/
│   │   ├── lib.rs             # IPC command handlers, single-instance plugin & event orchestration
│   │   └── main.rs            # Windows / Linux / macOS application entrypoint
│   ├── capabilities/          # Tauri 2 permissions (dialog, fs, core)
│   └── tauri.conf.json        # Window effects (Mica/Acrylic), app metadata & plugin config
├── frontend/                  # Modern React 19 + Vite + Tailwind CSS v4 frontend
│   └── src/
│       ├── components/
│       │   ├── LiveEditor.tsx # Single-canvas in-place WYSIWYG editor
│       │   ├── Editor.tsx     # Native dual-pane raw source editor
│       │   ├── Preview.tsx    # Standalone rich-text preview renderer
│       │   ├── TabBar.tsx     # Multi-tab management
│       │   ├── Toolbar.tsx    # Formatting toolbar & view switcher
│       │   ├── Outline.tsx    # Table of contents (TOC) drawer with smooth anchor scrolling
│       │   ├── StatusBar.tsx  # Word counts, character statistics, encoding & line/column status
│       │   ├── CommandPalette.tsx # Global command palette (Ctrl+K)
│       │   └── SaveConfirmModal.tsx # Unsaved changes confirmation dialog (Save/Don't Save/Cancel)
│       ├── utils/             # Markdown parser, KaTeX math & Mermaid rendering engine
│       └── App.tsx            # Global state coordinator, shortcuts & window event manager
└── tools/                     # Packaging & cross-platform build automation scripts
```

---

## Building from Source

### Prerequisites
- **Rust** 1.85+ (`rustc --version`)
- **Node.js** 20+ and **pnpm** 9+ (`pnpm --version`)
- Windows 10/11, or Linux (with `webkit2gtk-4.1` development packages installed)

### 1. Clone the Repository
```bash
git clone https://github.com/Speechlessmanbilibili/Yanbai.git
cd Yanbai
```

### 2. Run Rust Core Unit Tests
```bash
cargo test --workspace
```

### 3. Install Frontend Dependencies and Start Dev Server
```bash
pnpm --prefix frontend install
pnpm --prefix frontend dev
```

### 4. Build Release Binaries
```bash
# Build frontend production bundle
pnpm --prefix frontend build

# Build Tauri desktop release binary
cargo build --release --manifest-path src-tauri/Cargo.toml
```

Compiled binaries will be generated under `target/release/`.

---

## Copyright & License

This is not an open-source project, and the source code is not public. The builds published on [Yanbai-Releases](https://github.com/Speechlessmanbilibili/Yanbai-Releases) are distributed under the [Yanbai End User License Agreement](LICENSE.md) (Chinese version: [LICENSE_zh.md](LICENSE_zh.md)): you may download, install, and use them for personal or commercial purposes free of charge; redistributing, reselling, or publishing modified builds is not permitted.

Copyright © 2026 SilentPerson. All rights reserved.
