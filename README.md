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
- **Continuous live canvas**: read and write on a centered page with discreet editing cues. Click text, formatting, code, or formula symbols to edit at the corresponding source position; click away to restore the rendered view. Alt-click links to edit their text.
- **Rich content in place**: formulas, tables, code blocks, diagrams, and callouts render within the document and can be opened for editing.
- **Task lists**: display tasks and their completion state; enter editing to change the Markdown checkboxes.
- **Document links**: open HTTP(S), `mailto` and `tel` links in the system’s associated app; jump to anchors in the current document. Relative links open supported documents from the current document directory and reuse existing tabs. Save a new document before opening relative file links.
- **Protected embedded images**: protect embedded image bytes in all four views. In text editing areas, images appear as protected objects that can be copied or removed as a whole without editing their encoded content.
- **Paste and drop images**: insert PNG, JPEG, GIF, BMP, or WebP originals as short relative references. Saving copies images directly beside the document. Existing images with identical hashes are reused; different content prompts for a choice. The native save window includes a checked “Include image resources” option; clear it to save readable image placeholders.

### Document Engine Built in Pure Rust
- **Zero-dependency Word 97-2003 (.doc) parsing**: reads the OLE2 compound file directly, no Office or LibreOffice involved, and turns legacy `.doc` files into clean Markdown.
- **Bidirectional Word (.docx) conversion**: imports headings, formatting, lists, hyperlinks, and tables; exports standard OOXML with proper Chinese and Western typography.
- **Common text file editing and Save As**: open and save Markdown, JSON, YAML, TOML, CSV, HTML, code, and configuration files under their original extensions; Save As can also export Word (`.docx`).
- **Encoding-aware saving**: preserve the detected encoding and BOM, or choose “Save as UTF-8…” to convert explicitly. Invalid encoded text and characters the original encoding cannot represent produce an error. Saving, including Save As to the current file, checks external changes; Save As and Word/HTML export prevent overwriting another open document.
- **Session persistence and crash recovery**: debounced encrypted backups share identical content and save baselines in a content pool, preserving compatibility with older recovery files.

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
- **Windows integration**: optional `.md` / `.markdown` file association and an "Open with Yanbai" context menu entry, single-instance handling, and command-line file arguments.
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
| **macOS** | Apple silicon | `Yanbai-*-macos-arm64.dmg` | App installer image; no Developer ID signing or notarization |
| **macOS** | Apple silicon | `Yanbai-*-macos-arm64.app.tar.gz` | App archive with the same `Yanbai.app` as the matching `.dmg`; choose either |
| **macOS** | Intel | `Yanbai-*-macos-x64.dmg` | App installer image; no Developer ID signing or notarization |
| **macOS** | Intel | `Yanbai-*-macos-x64.app.tar.gz` | App archive with the same `Yanbai.app` as the matching `.dmg`; choose either |

**Windows**: run the installer, or unzip the portable package and start `Yanbai.exe`.

**Linux**: replace `<version>` with the version and `<arch>` with `x86_64` or `arm64` (choose `arm64` when `uname -m` reports `aarch64`), using the name of the downloaded file:

Replace `<version>` with the downloaded version. The commands select x86_64 or ARM64 from the current machine:

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

**macOS**: the `.dmg` and `.app.tar.gz` for the same architecture contain the same `Yanbai.app`; download either format. Open the `.dmg` and drag Yanbai to Applications, or extract `.app.tar.gz` and move `Yanbai.app` to Applications. Both formats use the same ad-hoc signing and have no Developer ID signature or notarization. If macOS blocks launch, follow [Apple’s instructions for opening an app from an unidentified developer](https://support.apple.com/102445).

---

## System Requirements

- **Windows** 10 or 11, x64 or ARM64.
- **Linux** x86_64 or aarch64 with the GTK 3 and `webkit2gtk-4.1` runtime libraries.
- **macOS** 11 (Big Sur) or later, Apple silicon or Intel; install system updates so the system WebKit is at Safari 16.4 or later. This minimum configuration has not been tested on a physical Mac.

---

## First launch and local data

First launch displays a native license window with the complete Chinese and English texts and prominent terms. “Accept and continue” atomically saves `license-acceptance.json` in the application data directory, recording the SHA-256 of both license texts, app version, acceptance time and displayed language, then opens the editor. An unchanged license is not asked about again because of an app version or interface language change. Changed text, a missing record or a damaged record requires confirmation again. The editor does not open if the record cannot be saved.

“Decline and exit”, closing the window or Escape exits without saving the refusal or creating the editor's WebView, preferences, logs, drafts or image cache. The prompt appears next time. Declining a new license does not clear existing data from an older version. Operating-system process records are outside the app's control.

The application data directory is `%APPDATA%/com.speechlessmanbilibili.yanbai` on Windows, `$XDG_DATA_HOME/com.speechlessmanbilibili.yanbai` on Linux (default `~/.local/share/com.speechlessmanbilibili.yanbai`), and `~/Library/Application Support/com.speechlessmanbilibili.yanbai` on macOS.

- Recovery drafts: only tabs with unsaved changes are backed up. They include text, saved baseline, encoding, file and image base directories, cursor and scroll positions, and other recovery state. Edits are backed up after about three seconds to locally encrypted `recovery.enc`; drafts are cleared when no unsaved changes remain or after a normal confirmed exit. Legacy `recovery.json` can still be migrated. Read, decryption or key errors preserve the original files and pause overwrite and cleanup.
- Recovery key: `recovery.key` is stored beside the draft and retained after normal exit. Windows protects it with the current user's DPAPI; Linux/macOS rely on local file permissions. Encryption does not replace device access control. Deleting a draft while editing does not turn off backup, and it may be recreated. Do not change or delete the key while the app is running.
- Image resources: originals pasted, dropped or imported from Word are staged in `image-resources` and reused by content hash; saving places resources beside the document according to “Include image resources”. Closing a document does not automatically delete the cache. You may clean it after exit, but images not yet saved beside a document and recovery drafts may still refer to it.
- Preferences and runtime caches: language, theme and view preferences use WebView local storage; the WebView also maintains its own profile and caches. These are separate from recovery drafts and are not cleared when documents close.
- Logs: local diagnostic logging starts after acceptance. It records runtime/framework diagnostics and does not deliberately record document text; error details may contain paths. The default rotates at about 40 KB per file and retains the current log and one previous log. Normal exit does not delete logs. Windows logs are in `%LOCALAPPDATA%/com.speechlessmanbilibili.yanbai/logs`, Linux logs are in `logs` under the application data directory above, and macOS logs are in `~/Library/Logs/com.speechlessmanbilibili.yanbai`.

The Software does not upload this local data. External image addresses in Markdown are retained, but the current app's content security policy blocks loading external images in the document, and saving does not download them. Actively opening external links may open a browser and cause network activity; standalone HTML exports also restrict external resources. Exit normally and back up needed documents and images before cleaning local files.

## Feedback

Found a bug or want a feature? Open an [issue](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues). Describe the steps that triggered the problem and, if you can, a minimal sample that reproduces it. Issues are public; consider a synthetic minimal sample or redaction. Feedback permissions and confidentiality terms are in Section 5 of the software license.

---

## Copyright & License

The official builds are distributed under the [Yanbai Software License](LICENSE.md) (Chinese version: [LICENSE_zh.md](LICENSE_zh.md)). Personal and commercial use, backups and internal deployment to affiliates, employees and contractors acting for your organization are free. External redistribution, sale, rental, public repository inclusion and bundled distribution require the Licensor's prior written permission; permitted internal deployment is exempt. The source code is not public, and this license grants no access to it. Third-party components and their own license terms are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

Copyright © 2026 SilentPerson. All rights reserved.

