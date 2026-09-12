<div align="center">

# Yanbai Markdown Editor

**A modern, in-place WYSIWYG bilingual Markdown editor built with Rust, Tauri 2.0, and React 19**

[![Release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?color=a85d3e&logo=github)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Speechlessmanbilibili/Yanbai-Releases/total?color=a85d3e)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases)

**English** | [简体中文](README_zh.md)

[Features](#key-features) • [Download & Installation](#download--installation) • [System Requirements](#system-requirements) • [Feedback](#feedback) • [Copyright & License](#copyright--license)

</div>

---

## Introduction

**Yanbai** (砚白) inherits a warm terracotta aesthetic, crafted for writers and creators who value focused typography and a pure writing flow. It is built on a pure Rust document engine and Tauri 2.0: a compact footprint (the standalone installer is about 13 MB), fast cold start, low memory use, and bidirectional Word interoperability that needs no Microsoft Office or LibreOffice installed.

This repository is the distribution point. It holds the installers, the prebuilt archives, and this page; the source code is not public.

---

## Key Features

### In-place Single-Canvas WYSIWYG
- **Immersive single-canvas writing**: no split panes, just a centered sheet of paper.
- **In-place render and edit**: formulas, tables, code blocks, diagrams, and callouts render in place. Click an element to edit it, click away to get the typeset result back.
- **Interactive task lists**: click a `- [ ]` checkbox in the rendered view and the Markdown source follows.

### Document Engine Built in Pure Rust
- **Zero-dependency Word 97-2003 (.doc) parsing**: reads the OLE2 compound file directly, no Office or LibreOffice involved, and turns legacy `.doc` files into clean Markdown.
- **Bidirectional Word (.docx) conversion**: imports headings, formatting, lists, hyperlinks, and tables; exports standard OOXML with proper Chinese and Western typography.
- **Multi-encoding detection**: BOM check, strict UTF-8 validation, and `chardetng` detection with a GBK fallback, plus SHA-256 fingerprinting so a file is never silently rewritten in the wrong encoding.
- **Session persistence and crash recovery**: debounced draft autosave with a 64 MB safety fuse.

### Academic and Visual Typography
- **KaTeX vector math**: inline `$E=mc^2$` and display blocks render in milliseconds.
- **Mermaid diagrams**: flowcharts, sequence diagrams, Gantt charts, class diagrams, state diagrams, and mindmaps out of the box.
- **Callout blocks**: the GitHub and Obsidian syntax for `[!NOTE]`, `[!TIP]`, `[!IMPORTANT]`, `[!WARNING]`, and `[!CAUTION]`.
- **Structured tables**: aligned and formatted without hand-tuning the pipes.

### Warm Terracotta Aesthetic and Desktop Integration
- **Warm terracotta palette** (primary `#a85d3e`, highlight `#e0a183`, ivory paper `#fdfbf7`) with light and dark themes.
- **Windows 11 Mica and Acrylic** window materials.
- **Multi-tab management**: unsaved-change dots, middle-click to close, and a confirmation dialog offering Save (S), Don't Save (D), or Cancel (Esc). `Ctrl+Shift+T` reopens recently closed tabs.
- **Windows integration**: optional `.md` / `.markdown` file association and an "Open with Yanbai" context menu entry, single-instance handling, and command-line file arguments.
- **Export**: Word (`.docx`), standalone offline HTML, and vector PDF printing.
- **Command palette**: `Ctrl+K` with fuzzy search over every action.

---

## Download & Installation

Grab the build for your platform from the [latest release](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest):

| Platform | Architecture | File | Notes |
| :--- | :--- | :--- | :--- |
| **Windows** | x64 | `Yanbai-*-win64-installer.exe` | Recommended. NSIS installer, can register file associations and the context menu entry |
| **Windows** | x64 | `Yanbai-*-win64.zip` | Portable, extract and run |
| **Windows** | ARM64 | `Yanbai-*-win-arm64-installer.exe` | NSIS installer for Windows on ARM, native ARM64 build |
| **Windows** | ARM64 | `Yanbai-*-win-arm64.zip` | Portable, extract and run |
| **Linux** | x86_64 | `Yanbai-*-linux-x86_64.tar.gz` | Prebuilt archive |
| **Linux** | ARM64 | `Yanbai-*-linux-arm64.tar.gz` | Prebuilt archive |

**Windows**: run the installer, or unzip the portable package and start `Yanbai.exe`.

**Linux**:

```bash
tar -xzf Yanbai-<version>-linux-x86_64.tar.gz
cd Yanbai-<version>-linux-x86_64
./run.sh
```

---

## System Requirements

- **Windows** 10 or 11, x64 or ARM64.
- **Linux** x86_64 or aarch64 with the GTK 3 and `webkit2gtk-4.1` runtime libraries.

---

## Feedback

Found a bug or want a feature? Open an [issue](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues). Crash reports are easier to act on when you include the document that triggered the problem, if it can be shared.

---

## Copyright & License

The builds in this repository are distributed under the [Yanbai End User License Agreement](LICENSE.md) (Chinese version: [LICENSE_zh.md](LICENSE_zh.md)): you may download, install, and use them for personal or commercial purposes free of charge; redistributing, reselling, or publishing modified builds is not permitted. The source code is not public, and this license grants no access to it. Third-party components and their own license terms are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

Copyright © 2026 SilentPerson. All rights reserved.
