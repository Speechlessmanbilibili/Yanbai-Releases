<div align="center">

<img src="https://raw.githubusercontent.com/Speechlessmanbilibili/Yanbai-Releases/main/assets/readme/icon.png" width="80" height="80" alt="Yanbai app icon">

# 砚白 · Yanbai

### Make room for the words.

A warm, focused workspace for Markdown.<br>Write on a continuous live canvas. Bring math and diagrams into the page. Move between Markdown and Word.

[![Latest release](https://img.shields.io/github/v/release/Speechlessmanbilibili/Yanbai-Releases?style=flat-square&color=a85d3e&label=Release)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)
![Platforms](https://img.shields.io/badge/Windows%20%C2%B7%20Linux%20%C2%B7%20macOS-a85d3e?style=flat-square)
[![Downloads](https://img.shields.io/github/downloads/Speechlessmanbilibili/Yanbai-Releases/total?style=flat-square&color=a85d3e)](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases)

**[Download Yanbai](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest)** · [Explore](#space-for-your-writing) · [Get started](#download--installation) · [Feedback](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues)

**English** | [简体中文](README_zh.md)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Speechlessmanbilibili/Yanbai-Releases/main/assets/readme/workspace-dark.png">
  <img src="https://raw.githubusercontent.com/Speechlessmanbilibili/Yanbai-Releases/main/assets/readme/workspace-light.png" alt="Yanbai Live view with continuous text, inline math, tasks, and a table in a warm, rounded workspace" width="1200">
</picture>

<sub>Actual Live view · Light and dark images follow your reading theme · Windows screenshot</sub>

</div>

---

## Space for your writing

| Write in context | Make ideas clear | Share your work |
| :--- | :--- | :--- |
| Edit styled text on a continuous page, with Markdown markers revealed at the cursor. | Bring formulas, diagrams, tables, and code into the same document. | Open Word files and export `.docx`, standalone HTML, or print to PDF. |

### Keep the thought moving

Bold, italic, highlight, and inline code stay styled as you type. Markdown markers appear when the cursor enters their range and hide when it leaves. Select across paragraphs, search and replace, and keep each document’s undo history as you switch tabs or editing views.

| View | Use it for |
| :--- | :--- |
| **Live** | Write and edit directly on a continuous, formatted page. |
| **Raw text** | Work directly with Markdown syntax. |
| **Split** | Keep Markdown and its preview side by side. |
| **Preview** | Read the rendered document. |

Split is the default; Yanbai remembers your selected view. The toolbar, context menu, shortcuts, command palette, and line-start `/` insertion give you the same editing tools, including when nothing is selected.

### Give complex content a clear shape

- **Math and diagrams**: KaTeX renders inline and display math; Mermaid supports flowcharts, sequence diagrams, Gantt charts, mindmaps, and more. Edit formula or diagram source alongside its preview.
- **Tables you can work in**: edit cells directly; insert, remove, move, and align rows or columns. Copy tables as Markdown, plain text, CSV, or HTML.
- **Details that belong in a document**: code highlighting and copying, task lists, callouts, footnotes, reference links, document properties, and collapsible sections.
- **Images beside your words**: paste or drop PNG, JPEG, GIF, BMP, or WebP. Save originals beside the document using relative references; matching content is reused, and conflicting files prompt for a choice.

### From an existing document to a finished draft

| Start with | Continue in Yanbai | Take it with you |
| :--- | :--- | :--- |
| Markdown and common text files | Edit with the original encoding and BOM; explicitly convert with “Save as UTF-8…” when needed. | Save text under its original extension. |
| Word `.doc` and `.docx` | Import headings, formatting, lists, links, tables, and images through the Rust document engine. | Export `.docx` without installing Office or LibreOffice. |
| Formulas, diagrams, and local images | Prepare the document in one workspace. | Export standalone HTML with complete formulas, diagrams, and supported embedded images, or print to PDF. |

Choose your line width and text size, follow the system’s light or dark appearance, and use Chinese or English throughout the interface. Tabs, outline, search, and a rounded canvas keep the workspace organized; reduced motion is available in Settings.

Saving checks for external file changes and protects other open documents from accidental overwrites. Local encrypted recovery drafts preserve unsaved work between interrupted sessions.

## Download & installation

Go to the [latest release](https://github.com/Speechlessmanbilibili/Yanbai-Releases/releases/latest) and choose your system and architecture. The `*` in the names below stands for a version such as `2.5.0`.

For Windows, most Intel/AMD PCs use x64; Windows on ARM devices use ARM64. For macOS, choose Apple silicon or Intel.

| Platform | Architecture | File | Use |
| :--- | :--- | :--- | :--- |
| **Windows** | x64 | `Yanbai-*-win64-installer.exe` | Installer · file associations |
| **Windows** | x64 | `Yanbai-*-win64.zip` | Portable archive |
| **Windows** | ARM64 | `Yanbai-*-win-arm64-installer.exe` | Native ARM64 installer |
| **Windows** | ARM64 | `Yanbai-*-win-arm64.zip` | Native ARM64 portable archive |
| **Linux** | x86_64 | `Yanbai-*-linux-x86_64.tar.gz` | Prebuilt archive |
| **Linux** | ARM64 | `Yanbai-*-linux-arm64.tar.gz` | Prebuilt archive |
| **macOS** | Apple silicon | `Yanbai-*-macos-arm64.dmg` | Drag to Applications |
| **macOS** | Apple silicon | `Yanbai-*-macos-arm64.app.tar.gz` | Same app, compressed archive |
| **macOS** | Intel | `Yanbai-*-macos-x64.dmg` | Drag to Applications |
| **macOS** | Intel | `Yanbai-*-macos-x64.app.tar.gz` | Same app, compressed archive |

### Windows

Run the installer, or extract the portable archive and open `Yanbai.exe`. The installer offers optional `.md` / `.markdown` file associations and an “Open with Yanbai” context menu entry.

### Linux

Download the archive for your machine and open a terminal in the download directory. Change only `<version>` in `version='<version>'` to the downloaded version number, such as `2.5.0`, without the `v` prefix. The commands use `uname -m` to detect the architecture automatically; no manual `arch` value is needed.

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

The `.dmg` and `.app.tar.gz` for the same architecture contain the same `Yanbai.app`; choose either. Open the `.dmg` and drag Yanbai to Applications, or extract `.app.tar.gz` and move `Yanbai.app` to Applications.

Both formats use ad-hoc signing, without Developer ID signing or notarization. If the system blocks launch, follow [Apple’s opening instructions](https://support.apple.com/102445).

### System requirements

- **Windows** 10 or 11, x64 or ARM64.
- **Linux** x86_64 or aarch64 with the GTK 3 and `webkit2gtk-4.1` runtime libraries.
- **macOS** 11 (Big Sur) or later, Apple silicon or Intel; install system updates so the system WebKit is at Safari 16.4 or later.

## A few useful moves

| To do this | Use this |
| :--- | :--- |
| Find an action | Open the command palette with `Ctrl+K`. |
| Insert content | Type `/` at the start of a line, or open the context menu. |
| Open a document link | In Live, use `Ctrl/Cmd + click`, middle-click, or `Ctrl/Cmd + Enter`; in Preview, click normally. |
| Edit a table | Click a cell; use `Tab` / `Shift+Tab` to move, and `Enter` / `Esc` to finish. |
| Reopen a tab | Use `Ctrl+Shift+T` for recently closed tabs in the current session. |

Anchors stay in the current document; relative file links use its directory. Save a new draft before opening a relative link. External links open through the system’s associated app.

## Your documents and local data

Documents are processed locally, with fonts, math, and diagram resources included in the app. First launch asks you to accept the software license and saves that decision before opening the editor. An unchanged license stays accepted across app updates and language changes.

The native save window defaults to “Include image resources”. Clear it to save a copy with readable image placeholders while retaining the full editing draft. Word and HTML exports can embed supported local or `data:` images.

<details>
<summary>Read more: first launch, recovery drafts, images, keys, and logs</summary>

First launch displays a native license window with the complete Chinese and English texts and prominent terms. “Accept and continue” atomically saves `license-acceptance.json` in the application data directory, recording the SHA-256 of both license texts, app version, acceptance time and displayed language, then opens the editor. An unchanged license is not asked about again because of an app version or interface language change. Changed text, a missing record or a damaged record requires confirmation again. The editor does not open if the record cannot be saved.

“Decline and exit”, closing the window or Escape exits without saving the refusal or creating the editor’s WebView, preferences, logs, drafts or image cache. The prompt appears next time. Declining a new license does not clear existing data from an older version. Operating-system process records are outside the app's control.

The application data directory is `%APPDATA%/com.speechlessmanbilibili.yanbai` on Windows, `$XDG_DATA_HOME/com.speechlessmanbilibili.yanbai` on Linux (default `~/.local/share/com.speechlessmanbilibili.yanbai`), and `~/Library/Application Support/com.speechlessmanbilibili.yanbai` on macOS.

- Recovery drafts: only tabs with unsaved changes are backed up. They include text, saved baseline, encoding, file and image base directories, cursor and scroll positions, and other recovery state. Edits are backed up after about three seconds to locally encrypted `recovery.enc`; drafts are cleared when no unsaved changes remain or after a normal confirmed exit. Legacy `recovery.json` can still be migrated. Read, decryption or key errors preserve the original files and pause overwrite and cleanup.
- Recovery key: `recovery.key` is stored beside the draft and retained after normal exit. Windows protects it with the current user’s DPAPI; Linux/macOS rely on local file permissions. Encryption does not replace device access control. Deleting a draft while editing does not turn off backup, and it may be recreated. Do not change or delete the key while the app is running.
- Image resources: originals pasted, dropped or imported from Word are staged in `image-resources` and reused by content hash; saving places resources beside the document according to “Include image resources”. Closing a document does not automatically delete the cache. You may clean it after exit, but images not yet saved beside a document and recovery drafts may still refer to it.
- Preferences and runtime caches: language, theme and view preferences use WebView local storage; the WebView also maintains its own profile and caches. These are separate from recovery drafts and are not cleared when documents close.
- Logs: local diagnostic logging starts after acceptance. It records runtime/framework diagnostics and does not deliberately record document text; error details may contain paths. The default rotates at about 40 KB per file and retains the current log and one previous log. Normal exit does not delete logs. Windows logs are in `%LOCALAPPDATA%/com.speechlessmanbilibili.yanbai/logs`, Linux logs are in `logs` under the application data directory above, and macOS logs are in `~/Library/Logs/com.speechlessmanbilibili.yanbai`.

The Software does not upload this local data. External image addresses in Markdown are retained, but the current app's content security policy blocks loading external images in the document, and saving does not download them. Actively opening external links may open a browser and cause network activity; standalone HTML exports also restrict external resources. Exit normally and back up needed documents and images before cleaning local files.

</details>

## Feedback and ideas

Found a problem, or have an idea? Open an [issue](https://github.com/Speechlessmanbilibili/Yanbai-Releases/issues) with your steps, system, version, and a minimal sample when useful. Issues are public; consider a synthetic or redacted example. Feedback permissions and confidentiality terms are in Section 5 of the software license.

## License

Official builds use the [Yanbai Software License](LICENSE.md) ([Chinese version](LICENSE_zh.md)). Personal and commercial use, backups, and internal deployment to affiliates, employees, and contractors acting for your organization are free. External redistribution, sale, rental, public repository inclusion, and bundled distribution require the Licensor’s prior written permission; permitted internal deployment is exempt. The source code is not public, and this license grants no access to it.

Third-party components and their license terms are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

---

<div align="center">

A place for your ideas. A page for your work.

<sub>Copyright © 2026 SilentPerson. All rights reserved.</sub>

</div>
