# Kindle 5 (No Touch) — Jailbreak & KOReader Guide

> **Device:** Kindle 5 (D01200)  
> **Firmware:** 4.0.0 – 4.1.4  
> **Difficulty:** Intermediate  
> **Time:** ~45 minutes

---

## Overview

The Kindle 5 is nearly identical to the Kindle 4 — same non-touch design, same navigation via 5-way joystick, very similar firmware. The jailbreak and setup process is the same as for the Kindle 4 with minor differences noted below.

**👉 Follow the [Kindle 4 guide](../kindle-4/README.md) as your primary reference.** This document only lists differences.

---

## Identifying Your Device

- Serial Number starts with `B00F` or `B011`
- Device Info: *Home → Menu → Settings → Device Info*
- Model name: **Kindle (5th Generation)**

---

## Differences from Kindle 4

| Aspect | Kindle 4 | Kindle 5 |
|---|---|---|
| Codename | D01100 | D01200 |
| Serial prefix | B006, B00A | B00F, B011 |
| Jailbreak file | `_k4_` in filename | `_k4_` also works (same FW line) |
| KOReader package | `kindle` | `kindle` |
| Navigation | 5-way + keyboard | 5-way + keyboard (identical) |

- The Kindle 5 uses the same firmware series (4.x) as the Kindle 4
- Use the same jailbreak files from [kindlemodding.org — K4 Legacy Jailbreak](https://kindlemodding.org/jailbreaking/Legacy/K4-Jailbreak)
- All steps (MKK, Keystore Update, KUAL, BlockAmazon, KOReader) are identical
- The same WiFi-in-foreground limitation applies

---

## Step-by-Step

Follow **all steps** from the [Kindle 4 guide](../kindle-4/README.md):

1. Prerequisites & file downloads
2. Jailbreak (same files, same diagnostic mode method)
3. MKK install
4. **Keystore Update 2025** (same — still critical!)
5. KUAL install
6. Block Amazon
7. KOReader v2026.03 (`kindle` package)
8. Calibre-Web OPDS
9. SSH server (port 2222)

---

## Resources

- [kindlemodding.org — K4/K5 Jailbreak](https://kindlemodding.org/jailbreaking/Legacy/K4-Jailbreak)
- [MobileRead Kindle 5 section](https://www.mobileread.com/forums/forumdisplay.php?f=145)
- [KOReader releases](https://github.com/koreader/koreader/releases)

---

*See also: [Full Kindle 4 Guide](../kindle-4/README.md) | [KOReader Setup](../../koreader/README.md) | [Calibre-Web](../../calibre-web/README.md)*
