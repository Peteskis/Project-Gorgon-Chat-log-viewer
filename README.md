# Project Gorgon Live Chat log viewer   
( New Live version 1.2 Beta is now added: includes text-to-speech and defined search fields to trigger TTS based on specific text, player names, or channel names, ++) I will add a Youtube vid soon to show how easy it is to use

Special thanks to https://www.twitch.tv/zewtastic  for giving me more ideas to implement.


# 👉  **[Launch Viewer here](https://peteskis.github.io/Project-Gorgon-Chat-log-viewer/)**  

---

[![Donate](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://www.paypal.com/donate/buttons?type=S&fromManage=true)  It's a Free Chat Viewer so only donate if you feel like it

---

# Project Gorgon — Live Chat Log Viewer (single-file HTML)

A lightweight, local-first viewer for **Project Gorgon** chat logs — runs entirely in your browser from one HTML file.

It displays chat in a clean, scrollable window with auto-built **channel tabs** (e.g. `[Global]`, `[Help]`, `[Nearby]`, `[NPC Chatter]`), **search**, **live auto-refresh**, **alert rules**, **text-to-speech**, and per-channel colour customisation.

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
- ⬇️ **Auto-scroll** toggle (on by default)
- 🗜️ **Compact view** toggle
- ↕️ **Resizable chat window** (drag handle to adjust height; saved locally)
- 🧰 Left “Input” panel has its own **scrollbar** so you can scroll options without using the page scrollbar

### Live updating
- 🔁 **Auto-refresh** reads the selected log repeatedly and appends **only new lines** (incremental)
- ⏱️ Interval dropdown: **1s / 2s / 5s / 10s / 30s**
- ▶️ Defaults to “live” on load (**Auto-scroll ON**, **Auto-refresh ON**, **1s** interval) — change any setting anytime

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

### Alert rules (multi-rule automation)
Create multiple rules that trigger on **new incoming lines** in live mode.

Each rule can include:
- Scope: **Current tab** or **All channels**
- Optional filters: **Channel**, **Speaker**, **Phrase**
- Actions:
  - 🔊 **Speak** the message (TTS)
  - 🎵 **Play custom sound** (choose your own audio file per rule)
  - 🖍️ **Highlight triggering line**
  - 👤 **Highlight all messages from the speaker** (duration configurable)
- Per-rule **Highlight seconds** and **Cooldown seconds**
- Rules are saved locally in your browser

Also includes:
- 🙋 **Mentions / My name** quick toggle (comma-separated name list) with the same actions/duration/cooldown options
- ⏱️ **Arm from now** button (ignore old lines and only react to new ones)

### Text-to-speech (TTS)
- Voice + speed controls
- “Read aloud” can filter by **Speaker** and/or **Channel**
- **Live (from now)** mode: starts at the bottom and only reads new matching messages
- When a phrase/rule triggers, it can highlight for ~20 seconds (configurable via rules/mentions)

### Performance mode
- 🚀 **Performance mode** enables virtualized rendering for huge logs (renders only on-screen rows)
- Does **not** delete history — you can still scroll back through everything
- In Performance mode, long lines are abbreviated for speed, but:
  - Hover shows the full line tooltip
  - Click a message to see full content in a **Full message preview** (scrollable)

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
6. Add **Alert rules** (or Mentions) for speaking/highlighting/sounds on live chat.

---

## Browser support

### Folder picker + best live support
Works best in **Chrome / Edge / Brave / Opera** (Chromium browsers).

- The browser will ask permission to read the chosen folder.
- On future visits the app may remember the folder handle, but you may still need to click **Grant access**.

### Firefox / Safari
Folder picking and persistent file handles are limited, so live folder reading may not work the same way.
You can still use:
- **Load log file**, or
- **Drag & drop**

(The app shows an in-app note when folder mode isn’t supported.)

---

## Log format

The viewer expects lines similar to:


YY-MM-DD HH:MM:SS    [Channel] Name: message

Example:

26-02-07 00:00:04    [Global] Zewtastic: hello



<img width="1630" height="1201" alt="image" src="https://github.com/user-attachments/assets/067e8ef7-a167-4470-aab3-c053827bb329" />


