# Kindle 4 (No Touch) — Complete Jailbreak & KOReader Guide

> **Device:** Kindle 4 (D01100) — the small, light, buttonful one without a touchscreen  
> **Firmware:** 4.0.0 – 4.1.4  
> **Difficulty:** Intermediate  
> **Time:** ~45 minutes

---

## ⚠️ Before You Start — Read This

- **Do NOT deregister your device** from Amazon before or during this process. The jailbreak relies on the device being registered (or at least having been registered). Deregistering can break things in unexpected ways.
- **Do NOT let Amazon update your firmware** during this process. Put the device in Airplane Mode first.
- This guide is for the **non-touch Kindle 4 only** (codename D01100). It has a physical 5-way controller and keyboard buttons. If you have a Kindle 5 (D01200), the steps are nearly identical — see `../kindle-5/README.md`.
- Steps must be followed **in order**. Skipping steps (especially the Keystore Update) will cause KUAL to malfunction.

---

## Prerequisites

### Hardware
- Kindle 4 (No Touch), model **D01100**
  - Verify: *Home → Menu → Settings → Device Info* — Serial Number starts with `B006` or `B00A`
- Micro-USB cable (data transfer capable — not charge-only)
- A computer running Windows, macOS, or Linux

### Firmware Version
- Your firmware must be between **4.0.0 and 4.1.4**
- Check: *Home → Menu → Settings* — firmware version shown at bottom
- If you're on 4.1.4 already, great. If you're on an older version, that's fine too.
- **If Amazon pushed you to a newer firmware**, check MobileRead for current jailbreak status.

### Files to Download
Download all files **before starting**. Keep them organized in a folder:

1. **Jailbreak package** from [kindlemodding.org — K4 Legacy Jailbreak](https://kindlemodding.org/jailbreaking/Legacy/K4-Jailbreak)
   - `Update_jailbreak_0.13.N_k4_install.bin`
   - `Update_jailbreak_0.13.N_k4_uninstall.bin` *(keep as backup)*
   - `diagnostic_menu_helper.bin` *(needed to navigate to diagnostic mode)*

2. **MKK (Mobileread Kindlet Kit)** — from [MobileRead thread](https://www.mobileread.com/forums/showthread.php?t=233932)
   - `MKK-*-install.bin`

3. **Keystore Update 2025** — from [MobileRead thread #225030](https://www.mobileread.com/forums/showthread.php?t=225030) *(CRITICAL — see Step 3)*
   - `Update_KindleUnpack_*_install.bin` or equivalent keystore update file from that thread

4. **KUAL (Kindle Unified Application Launcher)** — 2025 build from [MobileRead KUAL thread](https://www.mobileread.com/forums/showthread.php?t=203326)
   - `Update_KUALBooklet_*_install.bin`

5. **kindle-kual-blockamazon** — from [MobileRead / NiLuJe's repo](https://www.mobileread.com/forums/showthread.php?t=187787)
   - `Update_block_amazon_*_install.bin`

6. **KOReader v2026.03** — from [KOReader GitHub Releases](https://github.com/koreader/koreader/releases)
   - File: `koreader-kindle-v2026.03.zip` ← **Important:** use the `kindle` package, NOT `kindle-legacy`

---

## Step 1: Jailbreak the Device

The jailbreak uses the **NiLuJe method** via the Kindle's built-in diagnostic mode.

### 1.1 — Enter USB Disk Mode
1. Connect your Kindle to your computer via USB
2. On the Kindle, tap **Connect** when prompted (or it connects automatically)
3. The Kindle appears as a USB drive on your computer

### 1.2 — Copy the Jailbreak File
1. Open the Kindle USB drive
2. Copy `Update_jailbreak_0.13.N_k4_install.bin` to the **root** of the Kindle drive (not in any folder)
3. Also copy `diagnostic_menu_helper.bin` to the root

### 1.3 — Safely Eject
1. Safely eject/unmount the Kindle from your computer
2. The Kindle returns to its Home screen

### 1.4 — Enter Diagnostic Mode
> ⚠️ Navigation on the Kindle 4 is via the **5-way joystick** (up/down/left/right) and the **center button** to confirm. There is no touchscreen.

1. On the Home screen, press the **keyboard button** (bottom-left, looks like a grid)
2. Type: `~ds` (tilde, then d, then s) — this opens the diagnostics launcher
3. A menu appears. Navigate with the **5-way joystick** to highlight **"Run Diagnostic"** (or similar)
4. Press **center** to confirm
5. You should see a diagnostic screen. Navigate to the **Update** section
6. Select **"Update Your Kindle"** — this will run the jailbreak `.bin` file

> **Alternative if `~ds` doesn't work:** Some firmware versions require using the `diagnostic_menu_helper.bin` approach — install it via *Menu → Settings → Update Your Kindle* first.

### 1.5 — Verify Jailbreak Success
After the update process completes and the Kindle restarts:
1. Navigate to *Home → Menu → Settings → Device Info*
2. Look for a line that says: **"You are Jailbroken"** at the bottom of the info screen

✅ If you see **"You are Jailbroken"** — proceed to Step 2.  
❌ If you do NOT see it — do not continue. Check the MobileRead thread for troubleshooting.

---

## Step 2: Install MKK (Mobileread Kindlet Kit)

MKK provides the Java runtime environment needed to run Kindlets (third-party apps like KUAL).

### 2.1 — Copy MKK to Kindle
1. Connect Kindle via USB
2. Copy `MKK-*-install.bin` to the root of the Kindle drive
3. Safely eject

### 2.2 — Install via Settings
1. On the Kindle: *Home → Menu → Settings*
2. Press **Menu** again → select **"Update Your Kindle"**
3. Confirm the update
4. Kindle will restart after installation

✅ MKK is now installed. The Kindlet runtime is ready.

---

## Step 3: Keystore Update 2025 (CRITICAL ⚠️)

> **Why this is critical:** Without this step, when you open KUAL later it will show **"Kindlet Kit not installed"** — even though MKK is installed. This is a known issue with Kindle 4 firmware and Java keystores. The 2025 keystore update fixes the signing certificate chain.

### 3.1 — Get the File
- Go to [MobileRead thread #225030](https://www.mobileread.com/forums/showthread.php?t=225030)
- Download the keystore update `.bin` file from that thread (posted by NiLuJe or trusted contributors)
- File is typically named something like `Update_KindleUnpack_*_k4_install.bin`

### 3.2 — Install
1. Connect Kindle via USB
2. Copy the keystore update `.bin` to the root of the Kindle drive
3. Safely eject
4. On Kindle: *Menu → Settings → Update Your Kindle*
5. Confirm — device will restart

✅ Keystore updated. KUAL will now recognize MKK correctly.

---

## Step 4: Install KUAL (Kindle Unified Application Launcher)

KUAL is the launcher that lets you run KOReader and other extensions from a single, simple interface.

### 4.1 — Copy and Install
1. Connect Kindle via USB
2. Copy `Update_KUALBooklet_*_install.bin` to the root of the Kindle drive
3. Safely eject
4. On Kindle: *Menu → Settings → Update Your Kindle*
5. Confirm — device will restart

### 4.2 — Verify KUAL
1. Return to the Home screen
2. You should see a book icon named **"KUAL"** in your library
3. Open it — KUAL should launch and show a menu (may be empty for now)

✅ If KUAL opens without errors — proceed.  
❌ If KUAL shows "Kindlet Kit not installed" — go back to Step 3 and ensure the keystore update was applied.

---

## Step 5: Block Amazon Updates (kindle-kual-blockamazon)

> **Why:** Amazon can push OTA firmware updates that will un-jailbreak your device and wipe your KOReader installation. Blocking this protects everything you've set up.
> 
> Additionally, the `blockamazon` extension **protects the keystore** from being overwritten by Amazon's update mechanism.

### 5.1 — Install as a KUAL Extension
1. Connect Kindle via USB
2. On the Kindle drive, navigate to (or create) the folder: `extensions/`
3. Extract the `kindle-kual-blockamazon` package into `extensions/blockamazon/`
   - The structure should be: `extensions/blockamazon/config.xml` (and other files)
4. Also copy the `.bin` installer if provided and run it via *Settings → Update Your Kindle*
5. Safely eject and reopen KUAL

### 5.2 — Activate Block
1. Open KUAL
2. Navigate to **"Block Amazon"** (or "BlockAmazon")
3. Select **"Block OTA Updates"** / **"Enable Block"**
4. Confirm

✅ Amazon OTA updates are now blocked.

---

## Step 6: Install KOReader v2026.03

> **Package naming note:** There are two KOReader packages for Kindle:
> - `koreader-kindle-*.zip` ← **USE THIS ONE** for Kindle 4 (and most modern Kindle jailbreaks)
> - `koreader-kindle-legacy-*.zip` ← **Do NOT use** this — it's for very old firmware that lacks certain system libraries. Using the legacy package on a K4 will cause crashes or missing features.

### 6.1 — Extract KOReader
1. Connect Kindle via USB
2. On the Kindle drive, extract `koreader-kindle-v2026.03.zip`
3. This creates a folder `koreader/` in the root of the Kindle drive — this is correct
4. Also extract any required KUAL extension files for KOReader (the zip may include an `extensions/` folder — if so, merge it with the existing `extensions/` folder)

### 6.2 — Safely Eject and Launch
1. Safely eject the Kindle
2. Open KUAL on the Kindle
3. You should see **"KOReader"** in the KUAL menu
4. Press **center** to launch KOReader

### 6.3 — First Launch
- KOReader will load its own interface — very different from the stock Kindle UI
- Navigate with the **5-way joystick** + keyboard buttons
- Press **Menu** (in KOReader) to access settings
- To return to the Kindle home screen: use the **Home** button or *KOReader Menu → Exit*

✅ KOReader is installed and running!

---

## Step 7: Configure Calibre-Web OPDS in KOReader

OPDS (Open Publication Distribution System) is a protocol that lets KOReader browse and download from your Calibre-Web library over your local network.

> **File path note:** The OPDS configuration lives in `koreader/settings/opds.lua` on the Kindle drive. It does **NOT** live in `settings.reader.lua` — that's a common misconception. If you're editing config files manually, use the correct path.

### 7.1 — Prerequisites
- Calibre-Web must be running on your local network
- You need its IP address and port (e.g., `http://192.168.1.100:8083`)
- OPDS must be enabled in Calibre-Web: *Admin → Edit Basic Configuration → Feature Configuration → Enable OPDS*
- Note your Calibre-Web username and password

### 7.2 — Configure in KOReader
1. Open KOReader on your Kindle
2. From the file browser, press **Menu**
3. Navigate to **Search → OPDS Catalog**
   - (On some KOReader versions: *Tools → OPDS Catalog*)
4. Press **Add Catalog** (or the + icon)
5. Enter:
   - **Name:** My Calibre Library (or anything)
   - **URL:** `http://192.168.1.100:8083/opds` *(replace with your server's IP)*
   - **Username:** your Calibre-Web username
   - **Password:** your Calibre-Web password
6. Confirm / Save

### 7.3 — Browse and Download
1. Open the OPDS catalog you just added
2. Browse by author, title, or category
3. Navigate to a book and select **Download**
4. The book downloads directly to `/mnt/us/documents/` on your Kindle
5. It appears in KOReader's file browser immediately

### 7.4 — Manual Config Edit (Advanced)
If you need to edit OPDS settings manually:
```
/mnt/us/koreader/settings/opds.lua
```
This file contains your catalog list in Lua table format. Example entry:
```lua
{
    title = "My Calibre Library",
    url = "http://192.168.1.100:8083/opds",
    username = "admin",
    password = "yourpassword",
}
```
> ⚠️ **Do not** edit `settings.reader.lua` for OPDS — that file controls reader display preferences, not network catalogs.

---

## Step 8: SSH Server (Wireless Book Transfer)

KOReader includes a built-in SSH server that lets you push books wirelessly from your computer.

### 8.1 — Enable SSH in KOReader
1. Open KOReader
2. Press **Menu → Tools → SSH Server**
3. Enable the SSH server (toggle it on)
4. Note the IP address shown (your Kindle's WiFi IP)
5. Port is **2222** (not the standard 22)

> **Important:** WiFi on the Kindle 4 **only stays active while KOReader is in the foreground**. If you switch to the stock Kindle UI or the screen sleeps during file transfer, the WiFi connection will drop. Keep KOReader open and the screen awake during transfers.

### 8.2 — Connect from Your Computer
From your terminal (Linux/macOS) or PuTTY/WinSCP (Windows):

```bash
# List files on Kindle
ssh -p 2222 root@192.168.1.XXX

# Copy a book to Kindle (SCP)
scp -P 2222 mybook.epub root@192.168.1.XXX:/mnt/us/documents/

# Copy an entire folder
scp -P 2222 -r ~/Books/ root@192.168.1.XXX:/mnt/us/documents/
```

- **Username:** `root`
- **Password:** (empty by default, just press Enter — or check KOReader SSH settings)
- **Books go to:** `/mnt/us/documents/`

### 8.3 — Using rsync (Recommended for Large Libraries)
```bash
rsync -avz -e "ssh -p 2222" ~/Books/ root@192.168.1.XXX:/mnt/us/documents/
```

This only syncs changed/new files, making repeated transfers fast.

---

## Common Pitfalls & Troubleshooting

### 🕹️ Non-Touch Navigation
The Kindle 4 has **no touchscreen**. Navigation works as follows:
- **5-way joystick**: move cursor up/down/left/right
- **Center button**: confirm / open / select
- **Back button**: go back
- **Keyboard button**: open keyboard / type
- **Menu button**: context menu
- **Home button**: return to stock Kindle home screen

In KOReader, most functions are accessible via the Menu button + joystick. Take time to explore the menus — it's different from the stock Kindle UI but powerful once learned.

### 📶 WiFi Disconnects When KOReader is in Background
The Kindle 4's WiFi driver has a quirk: **WiFi only stays active when KOReader is actively running in the foreground**. This means:
- Don't switch to Home screen during OPDS downloads or SSH transfers
- Don't let the screen sleep during transfers (adjust sleep timeout temporarily)
- If the transfer drops, reconnect and resume (rsync handles this gracefully)

### 🔑 "Kindlet Kit not installed" in KUAL
This means the **Keystore Update** (Step 3) was not applied or failed. Solution:
1. Re-download the keystore update from [MobileRead thread #225030](https://www.mobileread.com/forums/showthread.php?t=225030)
2. Install it again via *Settings → Update Your Kindle*
3. Restart the Kindle fully (hold power for 7 seconds until it turns off, then press again)
4. Re-open KUAL

### 🚫 Do NOT Deregister from Amazon
Deregistering your Kindle from Amazon **can break the jailbreak** and cause signing issues. Leave the device registered (even if you never use Amazon's bookstore again). You can still block all Amazon network traffic via `blockamazon`.

### ⚡ Kindle Doesn't Show "Update Your Kindle" Option
This means no valid `.bin` file is present in the root of the drive. Double-check:
- The file is in the **root** (not inside a folder)
- The filename ends in `_install.bin`
- The file was copied before you ejected

### 💾 KOReader Shows "No Books"
Books must be in `/mnt/us/documents/` (the root of the Kindle's Documents folder). KOReader will also scan subdirectories. If you just added books via USB, you may need to refresh the file browser (Menu → Refresh).

---

## Summary — Installation Order

| Step | What | Why Order Matters |
|---|---|---|
| 1 | Jailbreak | Must be first — nothing works without it |
| 2 | MKK | Java runtime needed before KUAL |
| 3 | Keystore Update | Must happen after MKK, before KUAL |
| 4 | KUAL | Launcher for all extensions |
| 5 | Block Amazon | Protect your setup ASAP |
| 6 | KOReader | Main reader app |
| 7 | Calibre-Web OPDS | Library access (optional) |
| 8 | SSH Server | Wireless transfers (optional) |

---

## Next Steps

- 📚 Set up your Calibre-Web server: see [`../../calibre-web/README.md`](../../calibre-web/README.md)
- ⚙️ Customize KOReader: see [`../../koreader/README.md`](../../koreader/README.md)
- 🤝 Something unclear? Open an Issue!

---

*Guide maintained by the Kindle Revival community. Last verified with KOReader v2026.03 and K4 FW 4.1.4.*
