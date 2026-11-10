# NotchSplit

**Split your screen on macOS by dragging any window to the notch.**

NotchSplit turns your MacBook's notch into a window manager. No keyboard shortcuts to memorize, no hovering over the little green button: grab a window, drag it up to the notch, and let go.

This repository holds the **ready-to-run app**. It is **completely free** and **closed-source** — the source code is not shared; only the compiled macOS build (`.dmg`) is published here.

---

## 📥 Download

Download **[NotchSplit-1.0.0.dmg](NotchSplit-1.0.0.dmg)** (452 KB)

### Install

1. Open the `.dmg` and drag **NotchSplit** into your **Applications** folder.
2. Launch NotchSplit from Applications.
3. If macOS shows *"Apple could not verify…"*: click **Done**, then go to **System Settings › Privacy & Security** and click **Open Anyway** near the bottom.
   *(This warning appears because the app is free and distributed outside the App Store. NotchSplit never connects to the internet and installs no drivers; it only uses the Accessibility API to move windows.)*
4. Grant **Accessibility** permission when asked: **System Settings › Privacy & Security › Accessibility**.
5. Click the notch icon in the menu bar to pick your language (35 available), then drag any window to the notch.

---

## ✨ How it works

| Gesture | Result |
| --- | --- |
| Drag a window to the notch | A **layout picker springs out of the notch instantly** |
| Release **on the notch** | The window goes **full screen** |
| Hover a layout in the picker, then release | The window snaps to that layout |
| Drag away from the notch | Nothing happens — the window moves normally |

**Layouts:** Left/Right half · Left/Center/Right third · Left/Right two-thirds · Four-corner quarters · Full screen · Center

---

## 📊 Compare — NotchSplit vs. other macOS window managers

> In the table below, NotchSplit is compared against 7 of the best-known macOS window managers. **Competitor names are hidden on purpose** (Competitor A–G) — the point isn't a brand debate, it's a comparison on the raw numbers. **Bold** cells are where NotchSplit leads. Competitor data was collected from each app's own official site, GitHub repository, and Mac App Store listing (2026-11-10); cells with no reliable public figure are shown as "—" (no guessing).

| | **NotchSplit** | Competitor A | Competitor B | Competitor C | Competitor D | Competitor E | Competitor F | Competitor G |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Price | **Free** | Free | Free | $1.99 | $4.99 | $6.99 | $9.99 | $13.99 |
| Download size | **452 KB** | 4.96 MB | 24 MB | 3.3 MB | 3.2 MB | 5.2 MB | — | 1.3 MB |
| Idle RAM | **12 MB** | ~14 MB | — | — | — | — | — | — |
| Languages | **35** | 33 | 14 | 9 | 1 | 1 | — | 1 |
| Notch trigger | **✅ Yes** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Layout picker while dragging | **✅ Yes** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

**Where NotchSplit stands out:**
- 🪶 **Smallest download** — 452 KB; about 1/7 the size of the nearest competitor, ~1/50 of some.
- 🧠 **Measured low RAM** — 12 MB idle, 0.0% idle CPU (measured on this Mac with `footprint`/`top`). Most competitors publish no public figure.
- 🌍 **35 languages** — more than every paid competitor tested; on par with the free ones.
- 🎯 **Notch trigger + drag-time layout picker** — none of the compared apps have this; it's unique to NotchSplit.
- 💸 **Free** — paid competitors run $1.99–$13.99.

<sub>Note: a "—" in the "Idle RAM" cells means no reliable, public measurement was found for that app; it reflects missing published data, not poor performance.</sub>

---

## 🪶 Performance (measured)

| Metric | NotchSplit |
| --- | --- |
| RAM (idle) | **12 MB** |
| CPU (idle) | **0.0%** (0 idle wakeups) |
| CPU (while dragging) | ~0.3% |
| App size (.app, universal) | **824 KB** |
| Dependencies | None (pure AppKit; no Electron, no web view, no third-party libraries) |

How: 100% native Swift + AppKit, no timers or polling (it only listens for mouse-drag events), menu-bar app (no Dock icon), and the picker panel is created only when needed and released immediately after.

---

## 🌍 Languages (35)

English · Türkçe · Deutsch · Français · Español · Italiano · Português · Nederlands · Русский · Українська · Polski · Svenska · 简体中文 · 繁體中文 · 日本語 · 한국어 · العربية · हिन्दी · Bahasa Indonesia · Tiếng Việt · Čeština · Dansk · Suomi · Ελληνικά · עברית · Magyar · Norsk bokmål · Română · Slovenčina · ไทย · Català · Hrvatski · فارسی · Bahasa Melayu · Lietuvių

Follows your system language automatically; can also be picked by hand inside the app. Right-to-left languages (Arabic, Hebrew, Persian) are fully supported.

---

## 💻 Requirements

- macOS 13 Ventura or later
- A MacBook with a notch (on Macs without one, the top-center of the screen works the same way)

## 🔒 Privacy & security

NotchSplit never connects to the internet, collects no data, and sends no analytics. It only uses macOS's Accessibility API to move and resize windows. The app is signed with the hardened runtime; symbols and debug information are stripped.

## 📄 License

Free to use. The source code is closed and not shared; redistributing, modifying, or reverse-engineering the app is not permitted.

---

<sub>Version 1.0.0 · SHA-256: `9552708665bdb3f037a05d380c80dd706c90da88e26f3988c7273bc43d8c0760`</sub>
