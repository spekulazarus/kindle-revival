# Kindle Touch — Jailbreak & KOReader Guide

> **Device:** Kindle Touch (D01400 / S11)  
> **Firmware:** 5.x  
> **Difficulty:** Intermediate  
> **Time:** ~45 minutes

---

## Overview

The Kindle Touch was the first touchscreen Kindle. It runs firmware 5.x, which means the jailbreak method and some tooling differ from the Kindle 4/5 (which use 4.x). However, the end result is the same: KUAL + KOReader + Calibre-Web OPDS.

---

## Identifying Your Device

- Serial Number starts with `B00E` (D01400) or `B010`
- Has a touchscreen (infrared, not capacitive)
- Has no physical keyboard row, but has Home, Menu, and Back buttons
- Device Info: *Home → Menu → Settings → Device Info*

---

## Key Differences from Kindle 4/5

| Aspect | Kindle 4/5 | Kindle Touch |
|---|---|---|
| Firmware | 4.x | 5.x |
| Navigation | 5-way joystick | Touchscreen |
| Jailbreak source | kindlemodding.org Legacy K4 | kindlemodding.org Legacy Touch |
| Jailbreak method | Diagnostic mode | Update file method |
| KOReader package | `kindle` | `kindle` |

---

## Jailbreak

1. Go to [kindlemodding.org — Touch Jailbreak](https://kindlemodding.org/jailbreaking/Legacy/)
2. Download the appropriate files for the Kindle Touch / 5.x firmware
3. Copy the `_install.bin` file to the root of your Kindle drive
4. On Kindle: *Menu → Settings → Menu → Update Your Kindle*
5. The device restarts with jailbreak applied
6. Verify: *Settings → Device Info* → look for **"You are Jailbroken"**

---

## After Jailbreak

Follow the same pattern as the Kindle 4 guide:

1. ✅ **Jailbreak** (method above)
2. **MKK** — install Mobileread Kindlet Kit
3. **Keystore Update 2025** — from [MobileRead thread #225030](https://www.mobileread.com/forums/showthread.php?t=225030) — still required!
4. **KUAL** — install launcher
5. **Block Amazon** — protect your setup
6. **KOReader** — use `koreader-kindle-*.zip` (not legacy)
7. **Calibre-Web OPDS** — config in `koreader/settings/opds.lua`
8. **SSH server** — port 2222, push to `/mnt/us/documents/`

---

## Navigation in KOReader (Touch)

Unlike the Kindle 4/5, you can use the **touchscreen** in KOReader:
- Tap left edge: previous page
- Tap right edge: next page
- Tap center: show menu
- Swipe up/down: scroll in menus

---

## Resources

- [kindlemodding.org — Legacy Jailbreaks](https://kindlemodding.org/jailbreaking/Legacy/)
- [MobileRead Kindle Touch section](https://www.mobileread.com/forums/forumdisplay.php?f=140)
- [KOReader releases](https://github.com/koreader/koreader/releases)

---

*See also: [Full Kindle 4 Guide](../kindle-4/README.md) | [KOReader Setup](../../koreader/README.md) | [Calibre-Web](../../calibre-web/README.md)*
