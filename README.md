# 📚 Kindle Revival — Bring Your Old Kindle Back to Life

> **Deutsch:** Diese Anleitung ist auf Englisch verfasst, aber du kannst gerne Issues auf Deutsch erstellen. Wir helfen gerne!

---

## Overview

**Kindle Revival** is a community guide collection for breathing new life into old Amazon Kindle devices. Instead of letting your Kindle 4, 5, Touch, Keyboard, or Paperwhite 1 collect dust — or worse, buying new hardware — this project shows you how to:

- 🔓 **Jailbreak** your device (offline, no Amazon account needed)
- 📖 **Install KOReader** — a powerful, open-source e-book reader with EPUB, PDF, DJVU and much more
- 📚 **Connect Calibre-Web via OPDS** — browse and download your own library wirelessly
- 🔒 **Block Amazon** — prevent OTA updates from reverting your jailbreak
- 🔧 **SSH access** — push books directly from your computer over WiFi

No Amazon account. No subscriptions. Just your books, your device, your rules.

---

## Supported Devices

| Device | Codename | Firmware | Status |
|---|---|---|---|
| Kindle 4 (No Touch) | D01100 | 4.0.0 – 4.1.4 | ✅ Full Guide |
| Kindle 5 (No Touch) | D01200 | 4.0.0 – 4.1.4 | ✅ Guide Available |
| Kindle Touch | D01400 / S11 | 5.x | ✅ Guide Available |
| Kindle Keyboard (K3) | D00901 | 3.x | ✅ Guide Available |
| Kindle Paperwhite 1 | EY21 | 5.x | ✅ Guide Available |

> **Not sure which Kindle you have?** Go to *Settings → Device Info* (or *Menu → Settings → Device Info*) and check the Serial Number prefix.

---

## Quick Start

1. **Identify your device** using the table above
2. **Navigate to your device's folder** in `devices/`
3. **Follow the README step by step** — do not skip steps, order matters!
4. If you get stuck, open an Issue or check [MobileRead Forums](https://www.mobileread.com/forums/)

### General Requirements

- A USB cable (Micro-USB for most models)
- A computer (Windows / macOS / Linux all work)
- ~30 minutes of your time
- Your Kindle **must not be in Library mode** (use standard Home screen)

---

## What You Get

After completing the full setup:

### 🔓 Jailbreak
Your device is permanently unlocked. You can install third-party software (Kindlets) via **KUAL** (Kindle Unified Application Launcher).

### 📖 KOReader
A full-featured e-reader replacing (or sitting alongside) the stock reader:
- Supports EPUB, MOBI, PDF, DJVU, CBZ, FB2, and more
- Custom fonts, line spacing, hyphenation
- OPDS catalog client (connect to Calibre-Web directly!)
- Offline dictionary lookup
- SSH server for wireless file transfers

### 📚 Calibre-Web OPDS
Point KOReader at your self-hosted [Calibre-Web](https://github.com/janeczku/calibre-web) instance and browse/download your entire library — all on your local network, no cloud required.

### 🔒 Amazon Blocked
The `kindle-kual-blockamazon` extension prevents Amazon from pushing OTA firmware updates that would undo your jailbreak.

---

## Repository Structure

```
kindle-revival/
├── README.md                         ← You are here
├── devices/
│   ├── kindle-4/README.md            ← Kindle 4 full guide
│   ├── kindle-5/README.md            ← Kindle 5 guide
│   ├── kindle-touch/README.md        ← Kindle Touch guide
│   ├── kindle-keyboard/README.md     ← Kindle Keyboard (K3) guide
│   └── kindle-paperwhite-1/README.md ← Paperwhite 1 guide
├── calibre-web/README.md             ← Calibre-Web server setup
├── koreader/README.md                ← KOReader tips & config
└── scripts/README.md                 ← Helper scripts
```

---

## Contributing

Pull requests are welcome! If you have:
- A correction to an existing guide
- A guide for a device not yet covered
- A script that makes the process easier
- A translation (especially German 🇩🇪)

Please open a PR or an Issue. Let's keep old Kindles alive together. ♻️

---

## Resources & Credits

- [KOReader](https://koreader.rocks/) — the open-source e-reader
- [Calibre-Web](https://github.com/janeczku/calibre-web) — web-based Calibre library
- [MobileRead Forums](https://www.mobileread.com/forums/) — the heart of the Kindle modding community
- [kindlemodding.org](https://kindlemodding.org/) — modern jailbreak documentation
- [NiLuJe](https://www.mobileread.com/forums/member.php?u=69624) — the legend behind most Kindle tools

---

*Made with ❤️ for old hardware that still has plenty of life in it.*
