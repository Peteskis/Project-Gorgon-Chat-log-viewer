# Project Gorgon Chat log viewer   ( New Live version coming soon: includes text-to-speech and defined search fields to trigger TTS based on specific text, player names, or channel names.)

👉 **[Launch Viewer](https://peteskis.github.io/Project-Gorgon-Chat-log-viewer/)**  This is the older version that is an offline reader.


# Project Gorgon Chat Log Viewer (single-file HTML)

A lightweight, local-first viewer for **Project Gorgon** chat logs — runs entirely in your browser from one HTML file.

It displays chat in a clean, scrollable window with auto-built **channel tabs** (e.g. `[Global]`, `[Help]`, `[Nearby]`, `[NPC Chatter]`), **search**, **live auto-refresh**, **text-to-speech**, and per-channel colour customisation.

---

## Features

### Load your logs
- 📁 **Choose folder** (recommended, Chromium browsers) to browse log files in a folder
- 🔓 **Grant access** button to re-authorize a remembered folder handle (browser security requires a user click)
- 📄 **Load a single .log / .txt file**
- 🧲 **Drag & drop** log files onto the page
- 📋 **Paste log text** and parse it

### Viewing & navigation
- 🧭 **Channel tabs** automatically created from `[Channel]` tags  
  Includes an **All** tab and per-channel message counts
- 🔎 **Search** filters the currently selected tab
- ⬇️ **Auto-scroll** toggle
- 🗜️ **Compact view** toggle
- ↕️ **Resizable chat window** (drag handle to adjust height; saved locally)
- 🧰 Left “Input” panel has its own **scrollbar** so you can scroll options without using the page scrollbar

### Live updating
- 🔁 **Auto-refresh** reads the selected log repeatedly and appends **only new lines** (incremental)
- ⏱️ Interval dropdown: **1s / 2s / 5s / 10s / 30s**
- ▶️ Defaults to a “live” setup on load (**Auto-scroll ON**, **Auto-refresh ON**, **1s** interval) — change any setting anytime

### Colour system
- 🎨 Each channel gets a unique colour
  - Preset colours for common channels (e.g. Global/Help/Nearby/Status)
  - Unknown channels get a deterministic colour based on channel name
- 🧩 Colour applied consistently:
  - Message text tint
  - Speaker name colour
  - `[Channel]` pill colour
  - Subtle left-edge stripe on each row
- 🎛️ **Channel colour customisation UI** with colour picker + Clear  
  Saved locally and designed to stay smooth even with large logs

### Text-to-speech (TTS)
- 🔊 “Read aloud” panel:
  - Filter by **Speaker** (name before the `:`), **Channel**, or both
  - Optional **Trigger phrase** (e.g. `egg run`) to speak when anyone says it
  - **Scope**: Current tab (selected channel tab) or All channels
  - **Live (from now)** mode: starts at the bottom and only reads **new** matching messages
  - Voice and speed controls
- ✨ When a trigger phrase fires, the viewer **highlights all messages from the speaker** for **20 seconds** (and the triggering line is highlighted stronger)

### Privacy
- 🔒 **Nothing is uploaded** — parsing/viewing happens locally in your browser.

---

## How to use

1. Open the HTML (or GitHub Pages link) in your browser.
2. Load logs using one of:
   - **Choose folder** (recommended) → pick a log from the file list
   - **Load log file**
   - **Drag & drop** a log file onto the page
   - Paste text → **Parse Paste**
3. Click channel tabs to filter.
4. Use **Search** to filter the current tab.
5. Enable **Auto-refresh** for live updates (best with folder mode).

---

## Browser support

### Folder picker + best live support
Works best in **Chrome / Edge / Brave / Opera** (Chromium browsers).

- The browser will ask permission to read the chosen folder.
- On future visits the app may remember the folder handle, but you may still need to click **Grant access**.

### Firefox / Safari
These browsers do not support the same folder-handle API used for live folder reading.
You can still use:
- **Load log file**, or
- **Drag & drop**

(You’ll see an in-app note when folder mode isn’t supported.)

---
## Notes

Live” auto-refresh works best when the log file was selected via Choose folder, because it can keep a persistent handle to re-read the file efficiently.


## Log format

The viewer expects lines similar to:

YY-MM-DD HH:MM:SS    [Channel] Name: message

Example:

26-02-07 00:00:04    [Global] Zewtastic: hello



<img width="1630" height="1201" alt="image" src="https://github.com/user-attachments/assets/067e8ef7-a167-4470-aab3-c053827bb329" />





<img width="1618" height="1156" alt="image" src="https://github.com/user-attachments/assets/a61772b7-14c9-49f2-8071-b8248f8c4332" />

