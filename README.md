# Project Gorgon Chat log viewer

👉 **[Launch Viewer](https://peteskis.github.io/Project-Gorgon-Chat-log-viewer>/)**

A lightweight, local-first chat log viewer for **Project Gorgon** chat logs.

It displays chat in a clean viewer with channel tabs (e.g. `[Global]`, `[Help]`, `[Nearby]`), search, and per-channel colour customisation.

## Features

- 📁 Folder picker (Chrome / Edge / Brave) to browse logs in a chosen folder
- 📄 Load a single `.log` / `.txt` file (works in most browsers)
- 🧲 Drag & drop log files onto the page
- 🧭 Tabs automatically built from `[Channel]` tags in the log
- 🔎 Search (filters the current tab)
- 🎨 Per-channel colour picker (saved locally on your device)
- 🧾 Handles “system/status” lines (no speaker) cleanly
- 🔒 Privacy: nothing is uploaded — it runs in your browser

## How to use

1. Open the website link (GitHub Pages) in your browser.
2. Load your log using **one** of these:
   - **Choose folder** (recommended, Chromium browsers)
   - **Load log file**
   - Drag & drop a file onto the page
3. Click a channel tab to filter.

## Browser support

### Folder picker (Choose folder)
Works best in **Chrome / Edge / Brave**.

When you choose a folder, the browser will ask permission to read that folder.  
On future visits, the page may remember the folder handle, but you might still need to click **Grant access** depending on browser security rules.

### Other browsers (Firefox/Safari)
Folder picking may not be available. Use:
- **Load log file**, or
- drag & drop

## Log format

The viewer expects lines similar to:

`YY-MM-DD HH:MM:SS    [Channel] Name: message`

Example:

`26-02-07 00:00:04    [Global] Kanbe: hello`

Lines that don’t match are placed into an `Unparsed` channel so nothing is lost.

## Privacy

This project does **not** upload or transmit your log files anywhere.  
All parsing and viewing happens locally in your browser.

## Contributing / requests

Feel free to open an issue with:
- a sample (redacted) log snippet
- channel list you want styled by default
- feature requests (auto-load newest log, highlights, exports, etc.)
