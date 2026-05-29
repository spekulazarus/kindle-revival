# Kindle Paperwhite 1st Gen — Jailbreak & KOReader Guide

> **Device:** Kindle Paperwhite 1st Generation (EY21)  
> **Firmware:** 5.x  
> **Difficulty:** Intermediate  
> **Time:** ~45 minutes

---

## Overview

The Kindle Paperwhite 1 was the first Kindle with a **built-in frontlight**, making it excellent for reading in the dark. It runs firmware 5.x and has a capacitive touchscreen. KOReader supports the frontlight and gives you full control over brightness and warmth.

---

## Identifying Your Device

- Has a touchscreen with **built-in frontlight** (adjustable brightness)
- Serial Number starts with `B024` (WiFi) or `B01B` (3G)
- *Menu → Settings → Device Info* to confirm
- Model name: **Kindle Paperwhite (1st Generation)**

---

## Key Differences

| Aspect | Kindle 4 | Paperwhite 1 |
|---|---|---|
| Firmware | 4.x | 5.x |
| Screen | No touch, no light | Touch + frontlight |
| Navigation | 5-way joystick | Touchscreen |
| Jailbreak | K4 Legacy method | PW1-specific 5.x method |
| KOReader | `kindle` package | `kindle` package |

---

## Jailbreak

The Paperwhite 1 uses the **5.x jailbreak chain**:

1. Check current firmware: *Menu → Settings → Device Info*
2. Go to [kindlemodding.org — Paperwhite 1 / 5.x Jailbreak](https://kindlemodding.org/jailbreaking/)
3. Follow the current recommended method for your firmware version
   - For older 5.x: Direct `.bin` install method
   - For newer 5.x: May require the WinterBreak or similar exploit chain
4. Verify: *Settings → Device Info* → **"You are Jailbroken"**

> **Note:** Check the firmware version carefully. Newer PW1 firmware may require a different approach. Always check [MobileRead PW1 thread](https://www.mobileread.com/forums/showthread.php?t=245931) for the latest status.

---

## After Jailbreak

1. ✅ **Jailbreak**
2. **MKK** — Mobileread Kindlet Kit (same as K4)
3. **Keystore Update 2025** — [MobileRead thread #225030](https://www.mobileread.com/forums/showthread.php?t=225030)
4. **KUAL** — same KUAL package works
5. **Block Amazon** — highly recommended on 5.x devices
6. **KOReader** — `koreader-kindle-*.zip`
7. **Calibre-Web OPDS** — `koreader/settings/opds.lua`
8. **SSH server** — port 2222

---

## Frontlight in KOReader

KOReader controls the Paperwhite's frontlight natively:
- Swipe up/down on the **left edge**: adjust brightness
- *Menu → Screen → Frontlight*: full brightness and warmth controls
- You can schedule automatic brightness changes (e.g., dim at night)

---

## Resources

- [kindlemodding.org — Main Jailbreak Page](https://kindlemodding.org/jailbreaking/)
- [MobileRead Paperwhite section](https://www.mobileread.com/forums/forumdisplay.php?f=179)
- [KOReader releases](https://github.com/koreader/koreader/releases)

---

*See also: [Full Kindle 4 Guide](../kindle-4/README.md) | [KOReader Setup](../../koreader/README.md) | [Calibre-Web](../../calibre-web/README.md)*
