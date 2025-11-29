# AI Studio – Chat Viewer

A small single-file web app to browse **Google AI Studio** markdown exports, with:

- Folding for `<thinking>` blocks
- Global collapse/expand per conversation
- Light/dark theme
- Drag & drop for files and folders

> This is “vibe-coded” and runs 100% locally in your browser – no backend, no analytics.

---

## 1. Exporting from Google AI Studio

1. Install the **Violentmonkey** browser extension  
   👉 https://violentmonkey.github.io/

2. Create a new userscript and copy–paste the content of [`script_3.7.txt`](./script_3.7.txt).

3. Save and enable the script, then refresh Google AI Studio.  
   You should see **two new buttons** on a conversation:

   - `Export (.md)` – without `<thinking>`
   - `Export with thinking (.md)` – includes hidden `<thinking>` sections

4. Each button downloads a markdown file you can open with this viewer.

The script is a small modification of this original one:  
https://greasyfork.org/en/scripts/554502-google-ai-studio-conversation-chat-markdown-export-download-dom-based

---

## 2. Using the markdown viewer

1. Download [`aistudio_viewer_v1.html`](./aistudio_viewer_v1.html) (or the latest version).
2. Open it directly in your browser (double-click is enough).
3. In the app you can:

   - **Drag & drop** one or more `.md` files, or even a **folder** of exports
   - Use **“Open files”** / **“Open folder”** buttons if you don’t like drag & drop
   - Switch between **light / dark** mode
   - Click a header to **collapse a single interaction**
   - Click the **bubble** to collapse/expand all interactions in the file
   - Toggle visibility of `<thinking>` blocks with the **“Thinking”** button

---

## 3. Current features

- Sidebar with:
  - File list (supports folders / relative paths)
  - Search box to filter files
  - Quick rename of file labels (only inside the app, not on disk)

- Conversation view:
  - User prompts as **headers**
  - `<thinking>` blocks shown in a separate collapsible section
  - Global toggle for all `<thinking>` blocks
  - Adjustable “header size” for how much of the prompt is used as a title

- Export:
  - “Export mode” to select which interactions to include
  - Optional in-place editing of messages before export
  - Exported file keeps the same AI Studio markdown format

---

## 4. Limitations / notes

- Tested mainly with **Google AI Studio** exports produced by `script_3.7.txt`.
- Some unusual export formats might still break the parser (please open an issue with a sample file).
- Everything runs **locally** in the browser – nothing is sent anywhere.

---

## 5. Contributing / feedback

This is my first public coded project, mostly vibe coded irocinally using CHatGPT 5.1.  
Bug reports, suggestions or pull requests are very welcome!

- Open an issue: https://github.com/Watchy94/aistudio_viewer/issues
- Or just fork and experiment 🙂
