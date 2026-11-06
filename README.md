# prettySNow (`pSNo`)

[![Live Web App](https://img.shields.io/badge/Live_App-GitHub_Pages-38bdf8?style=flat-square&logo=github)](https://blainekyle.github.io/prettySNow/)
[![Latest Release](https://img.shields.io/badge/Release-v1.9cN_(Windows_x64_%2B_Offline_HTML)-10b981?style=flat-square)](https://github.com/blainekyle/prettySNow/releases/latest)

**Converts rich text and images into clean, self-contained ServiceNow inline `[code]` HTML.**

- **Launch Web App:** **[blainekyle.github.io/prettySNow](https://blainekyle.github.io/prettySNow/)**
- **Desktop & Offline Downloads:** **[GitHub Releases (`v1.9cN`)](https://github.com/blainekyle/prettySNow/releases/latest)** (`pSNo_1.9cN-win_x64.exe` portable Windows x64 Neutralino app & `pSNo-1.9cN.html` offline single-file build)

---

## Overview

ServiceNow journal fields (Additional Comments / Work Notes) accept inline HTML wrapped in `[code]...[/code]` tags, but pasting formatted content directly often produces broken markup, stripped styles, oversized image payloads, or unintended `<br>` line-break inflation.

**prettySNow (`pSNo`)** provides a side-by-side visual rich-text workspace and live ServiceNow HTML code editor with built-in Base64 image compression, comment recycling, and single-line "Krunched" export for environments where you want a standalone web or desktop tool (if you can install Chrome extensions and want direct Side Panel syncing with ServiceNow ticket fields, see [**Snowcow**](https://github.com/blainekyle/Snowcow)).

---

## Key Features

- **Dual-Pane Synchronized Workspace**:
  - **Left Pane (Rich Text Visual Editor):** Styled after ServiceNow portal typography with formatting controls (`B`, `I`, `H2`/`H3`/`P`, `<hr>`, hyperlinks, undo), **Semantic Cleanup (`Clean`)**, and **`View: Krunched`** spacing preview.
  - **Right Pane (Live ServiceNow HTML Editor):** Real-time HTML output and direct code editing with quick tag-insertion buttons (`<p>`, `<b>`, `<i>`, `<br>`, `<hr>`, `<a>`, `<ul>`, `<ol>`, `<li>`), **`B64: Show / Hide`** to collapse long Base64 image strings while editing, and **`SN Tags: ON / OFF`** to toggle `[code]...[/code]` wrappers.
  - **Collapsible Center Gutter (`◀` / `▶`):** Expand either editor full-width on demand.
- **Recycle ServiceNow Comments (`↻SN`)**: Paste existing HTML comments copied out of ServiceNow and normalize them back into clean, editable semantic paragraph blocks.
- **Built-In Image Super-Modal (`Add` & Batch `Process`)**:
  - Import images via **drag-and-drop**, **file picker (`📁Select`)**, direct **OS clipboard paste (`📋Paste`)**, or **remote URL-to-Base64 fetch (`🔗Convert`)** (or link an external image URL directly).
  - Aspect-ratio-locked **Width (`px`)** and **Quality (`10%–100%`)** sliders with real-time visual preview and payload size readout to keep inline Base64 strings compact.
  - Step through and re-compress all images already pasted into a document using **`Process`**.
- **Copy Code vs. Copy Krunched**:
  - **`Copy Code`** copies formatted, readable HTML.
  - **`Copy Krunched`** copies a single-line payload so ServiceNow journal parsers never inject unwanted `<br>` tags between indented HTML lines.
- **Hybrid Browser & Native Windows Desktop (`v1.9cN`)**:
  - Runs identically on GitHub Pages, completely offline from a single `.html` file (with embedded fonts), or as a lightweight ~4 MB borderless native Windows x64 desktop app (`pSNo_1.9cN-win_x64.exe`) built on Neutralinojs.
  - Includes a built-in slide-out **Manual (`🕮`)** and quick access to [**prettySNow Classic**](https://blainekyle.github.io/prettySNow/prettysnow.classic.html).
