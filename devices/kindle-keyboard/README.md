# Kindle Keyboard (K3) — Jailbreak & KOReader Guide

> **Device:** Kindle Keyboard, also known as Kindle 3 (K3), codename D00901  
> **Firmware:** 3.x  
> **Difficulty:** Intermediate  
> **Time:** ~45 minutes

---

## Overview

The Kindle Keyboard (3rd generation) is a beloved device with a full physical QWERTY keyboard. It runs firmware 3.x, which is the oldest firmware series still supported by modern KOReader and the jailbreak toolchain.

---

## Identifying Your Device

- Has a full QWERTY keyboard below the screen
- Serial Number starts with `B006` or similar K3 prefix
- *Menu → Settings → Device Info* to confirm model
- Comes in WiFi-only and 3G+WiFi variants

---

## Key Differences

| Aspect | Kindle 4 | Kindle Keyboard |
|---|---|---|
| Firmware | 4.x | 3.x |
| Navigation | 5-way joystick | 5-way joystick + full keyboard |
| Jailbreak source | K4 files | K3-specific files |
| Jailbreak method | Diagnostic mode | Update file or WPA2-CCMP |
| KOReader package | `kindle` | `kindle` |

---

## Jailbreak Methods

The Kindle Keyboard has **two jailbreak methods**:

### Method 1: Update File (Recommended)
1. Go to [kindlemodding.org — K3 Jailbreak](https://kindlemodding.org/jailbreaking/Legacy/)
2. Download K3-specific `_install.bin`
3. Copy to root of Kindle drive
4. *Menu → Settings → Menu → Update Your Kindle*

### Method 2: WPA2-CCMP (if firmware is too new)
- Some K3 firmware versions require the WiFi-based jailbreak
- Documented at [MobileRead K3 Jailbreak thread](https://www.mobileread.com/forums/showthread.php?t=88004)

---

## After Jailbreak

Same pattern as Kindle 4:

1. ✅ **Jailbreak**
2. **MKK** — Mobileread Kindlet Kit
3. **Keystore Update 2025** — [MobileRead thread #225030](https://www.mobileread.com/forums/showthread.php?t=225030) — critical!
4. **KUAL**
5. **Block Amazon**
6. **KOReader** — `koreader-kindle-*.zip`
7. **Calibre-Web OPDS** — `koreader/settings/opds.lua`
8. **SSH server** — port 2222

---

## Navigation in KOReader

The full keyboard makes KOReader navigation quite comfortable:
- **5-way joystick**: navigate menus
- **Q/W** or **Page Turn buttons**: previous/next page
- **Enter/Center**: confirm
- **Back button**: go back
- **Menu button**: KOReader menu

---

## Resources

- [kindlemodding.org — K3 Legacy Jailbreak](https://kindlemodding.org/jailbreaking/Legacy/)
- [MobileRead Kindle Keyboard section](https://www.mobileread.com/forums/forumdisplay.php?f=135)
- [KOReader releases](https://github.com/koreader/koreader/releases)

---

*See also: [Full Kindle 4 Guide](../kindle-4/README.md) | [KOReader Setup](../../koreader/README.md) | [Calibre-Web](../../calibre-web/README.md)*
