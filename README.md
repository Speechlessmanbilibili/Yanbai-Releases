<div align="center">

# Yanbai Markdown Editor

**A bilingual Markdown editor with four writing views, built with Rust, Tauri 2, and React 19**

[![Release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?color=a85d3e&logo=github)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Speechlessmanbilibili/Yanbai-Releases/total?color=a85d3e)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases)

**English** | [简体中文](README_zh.md)

[Features](#key-features) • [Download & Installation](#download--installation) • [System Requirements](#system-requirements) • [Feedback](#feedback) • [Copyright & License](#copyright--license)

</div>

---

## Introduction

**Yanbai** (砚白) combines a warm terracotta palette with focused typography. Choose a split editor and preview, edit on a continuous live canvas, work with Markdown text, or read the rendered document. Its Rust document engine supports Word import and export without Microsoft Office or LibreOffice.

This repository is the distribution point. It holds the installers, the prebuilt archives, and this page; the source code is not public.

---

## Key Features

### Four Writing Views

- **Split, Live, Raw text, and Preview**: start in Split view and restore your selected view on the next launch. Choosing Split returns to the default.
- **Continuous live canvas**: read and write on a centered page with discreet editing cues. Single-click plain text to place the cursor at that position; click away to restore its rendered appearance.
- **Rich content in place**: formulas, tables, code blocks, diagrams, and callouts render within the document and can be opened for editing.
- **Task lists**: display tasks and their completion state; enter editing to change the Markdown checkboxes.
- **Protected embedded images**: protect embedded image bytes in all four views. In text editing areas, images appear as protected objects that can be copied or removed as a whole without editing their encoded content.
- **Paste and drop images**: paste a clipboard image or drop a PNG, JPEG, GIF, BMP, or WebP file to embed its original bytes directly in the document. Saved documents do not depend on the original image files.

### Document Engine Built in Pure Rust
- **Zero-dependency Word 97-2003 (.doc) parsing**: reads the OLE2 compound file directly, no Office or LibreOffice involved, and turns legacy `.doc` files into clean Markdown.
- **Bidirectional Word (.docx) conversion**: imports headings, formatting, lists, hyperlinks, tables, and supported images; exports standard OOXML with Chinese and Western typography.
- **Text formats and Save As**: edit and save Markdown, JSON, YAML, TOML, CSV, HTML, and common source/configuration files under their original extensions; Save As can export Word (`.docx`). Imported Word files use Save As; an existing `.docx` is overwritten only after the user selects and confirms that path.
- **Encoding-aware saving**: preserve the detected encoding and BOM, or choose “Save as UTF-8…” to convert explicitly. Invalid encoded text and characters the original encoding cannot represent produce an error; external file changes are checked before saving.
- **Session persistence and crash recovery**: automatically back up drafts and show backup status, with a 64 MiB recovery-file limit.

### Academic and Visual Typography
- **KaTeX vector math**: inline `$E=mc^2$` and display blocks render in milliseconds.
- **Mermaid diagrams**: flowcharts, sequence diagrams, Gantt charts, class diagrams, state diagrams, and mindmaps out of the box.
- **Callout blocks**: the GitHub and Obsidian syntax for `[!NOTE]`, `[!TIP]`, `[!IMPORTANT]`, `[!WARNING]`, and `[!CAUTION]`.
- **Structured tables**: aligned and formatted without hand-tuning the pipes.

### Warm Terracotta Aesthetic and Desktop Integration
- **Chinese and English interface**: Settings uses the system language by default, or remembers Chinese or English. Licence terms are on a secondary settings page.
- **Warm terracotta palette** (primary `#a85d3e`, highlight `#e0a183`, ivory paper `#fdfbf7`) follows the system appearance by default. Choose Follow system, Light, or Dark in Settings; manual selections persist across restarts, and returning to Follow system clears the saved preference.
- **Windows 11 Mica and Acrylic** window materials.
- **Multi-tab management**: unsaved-change dots, middle-click to close, and a confirmation dialog offering Save (S), Don't Save (D), or Cancel (Esc). `Ctrl+Shift+T` reopens recently closed tabs.
- **Windows integration**: optional `.md` / `.markdown` file association and an “Open with Yanbai” context menu entry, single-instance handling, and command-line file arguments.
- **Export with embedded images**: Word (`.docx`) and standalone offline HTML embed supported local or `data:` images (PNG, JPEG, GIF, BMP, and WebP). Save web images locally and reference them from the document before exporting; SVG and unavailable images report an error. HTML exports include complete formulas and diagrams without rendering scripts. PDF printing is also available.
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
| **macOS** | Apple silicon | `Yanbai-*-macos-arm64.dmg` | Unsigned; right-click and Open on first launch |
| **macOS** | Intel | `Yanbai-*-macos-x64.dmg` | Unsigned; right-click and Open on first launch |

**Windows**: run the installer, or unzip the portable package and start `Yanbai.exe`.

**Linux**:

```bash
tar -xzf Yanbai-<version>-linux-x86_64.tar.gz
cd Yanbai-<version>-linux-x86_64
./run.sh
```

**macOS**: open the dmg and drag Yanbai into Applications. The builds are neither signed nor notarised, so Gatekeeper blocks the first launch: right-click the icon and choose Open, or run

```bash
xattr -dr com.apple.quarantine /Applications/Yanbai.app
```

If you would rather skip the dmg, `Yanbai-<version>-macos-<arch>.app.tar.gz` contains the `.app` itself.

---

## System Requirements

- **Windows** 10 or 11, x64 or ARM64.
- **Linux** x86_64 or aarch64 with the GTK 3 and `webkit2gtk-4.1` runtime libraries.
- **macOS** 10.13 or later, Apple silicon or Intel.

---

## Feedback

Found a bug or want a feature? Open an [issue](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues). Describe the steps that triggered the problem and, if you can, a minimal sample that reproduces it. Do not attach documents that contain confidential or personal information: issues are public, and the license treats feedback as non-confidential. Submitting an issue means you agree to the feedback license in [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Copyright & License

The builds in this repository are distributed under the [Yanbai End User License Agreement](LICENSE.md) (Chinese version: [LICENSE_zh.md](LICENSE_zh.md)): you may download, install, and use them for personal or commercial purposes free of charge; redistributing, reselling, or publishing modified builds is not permitted. The source code is not public, and this license grants no access to it. Third-party components and their own license terms are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). The installer shows this agreement before it copies any files. In the app, open Settings and select Licence and third-party notices to read the full text.

Copyright © 2026 SilentPerson. All rights reserved.
