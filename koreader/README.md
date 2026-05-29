# KOReader — Tips, Configuration & Customization

> Getting the most out of KOReader on your old Kindle

---

## Overview

[KOReader](https://koreader.rocks/) is a powerful open-source document viewer that supports EPUB, MOBI, PDF, DJVU, CBZ, FB2, TXT, HTML, and more. On old Kindles, it's a massive upgrade over the stock reader.

---

## Installation

See your device-specific guide for installation instructions:
- [Kindle 4](../devices/kindle-4/README.md)
- [Kindle 5](../devices/kindle-5/README.md)
- [Kindle Touch](../devices/kindle-touch/README.md)
- [Kindle Keyboard](../devices/kindle-keyboard/README.md)
- [Paperwhite 1](../devices/kindle-paperwhite-1/README.md)

---

## Key Features for Old Kindles

### EPUB Support
The stock Kindle reader doesn't support EPUB. KOReader does — and it renders EPUB beautifully with custom fonts, margins, and line spacing.

### OPDS Client
Browse and download from your Calibre-Web library wirelessly. See [Calibre-Web guide](../calibre-web/README.md).

### SSH Server
Push books over WiFi from your computer (port 2222).

### Custom Fonts
Copy `.ttf` or `.otf` font files to `/mnt/us/koreader/fonts/` and they become available in KOReader's font selector.

---

## Configuration Files

KOReader stores its config in `/mnt/us/koreader/settings/`:

| File | Purpose |
|---|---|
| `opds.lua` | OPDS catalog list (Calibre-Web, etc.) |
| `settings.reader.lua` | Reader display preferences |
| `statistics.sqlite3` | Reading statistics database |
| `vocabulary_builder.sqlite3` | Dictionary lookup history |

> ⚠️ Edit `opds.lua` for OPDS catalogs, **not** `settings.reader.lua`.

---

## Useful Gestures & Shortcuts

### Non-Touch Kindles (4/5/Keyboard)
- **5-way joystick**: Navigate menus and pages
- **Center button**: Select / open
- **Menu button**: Open KOReader main menu
- **Home button**: Exit KOReader (return to Kindle home)
- **Back button**: Previous screen/page

### Touch Kindles (Touch, Paperwhite)
- **Tap left edge**: Previous page
- **Tap right edge**: Next page
- **Tap center**: Show menu
- **Swipe left/right**: Turn pages
- **Swipe up/down (left edge)**: Brightness (Paperwhite only)

---

## WiFi Limitations on Old Kindles

On Kindle 4/5 and Keyboard:
- **WiFi only works while KOReader is in the foreground**
- Switching to the stock Kindle UI drops the WiFi connection
- This affects OPDS downloads and SSH transfers
- Keep KOReader open during any wireless activity

---

## Reading Statistics

KOReader tracks your reading time and progress. Access via:
*Menu → Tools → Reading Statistics*

---

## Dictionary Setup

1. Download a dictionary in StarDict format (`.ifo`, `.idx`, `.dict.dz`)
2. Copy to `/mnt/us/koreader/data/dict/`
3. In KOReader: *Menu → Settings → Dictionary* → select your dictionary
4. Long-press a word to look it up

---

## Updates

KOReader releases roughly every few months. To update:
1. Download the new `koreader-kindle-*.zip` from [GitHub Releases](https://github.com/koreader/koreader/releases)
2. Connect Kindle via USB
3. Extract and overwrite the `koreader/` folder on the Kindle drive
4. Your settings in `koreader/settings/` are preserved

---

## Resources

- [KOReader Website](https://koreader.rocks/)
- [KOReader GitHub](https://github.com/koreader/koreader)
- [KOReader Wiki](https://github.com/koreader/koreader/wiki)
- [MobileRead KOReader thread](https://www.mobileread.com/forums/showthread.php?t=215275)
