# Calibre-Web Setup Guide

> Self-host your ebook library and access it wirelessly from your Kindle via OPDS

---

## Overview

[Calibre-Web](https://github.com/janeczku/calibre-web) is a web application that provides a clean interface for your Calibre library. For Kindle Revival purposes, the key feature is its **OPDS catalog** — a standard protocol that KOReader can connect to for browsing and downloading books wirelessly.

---

## Requirements

- A computer or server on your **local network** that can run Python/Docker
- [Calibre](https://calibre-ebook.com/) for library management (optional but recommended)
- Your ebook collection organized in a Calibre library

---

## Installation Options

### Option A: Docker (Recommended)

```bash
docker run -d \
  --name=calibre-web \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Europe/Berlin \
  -p 8083:8083 \
  -v /path/to/config:/config \
  -v /path/to/books:/books \
  --restart unless-stopped \
  lscr.io/linuxserver/calibre-web:latest
```

Replace `/path/to/books` with the path to your Calibre library folder (the one containing `metadata.db`).

### Option B: Python (pip)

```bash
pip install calibreweb
cps
```

---

## Initial Configuration

1. Open `http://localhost:8083` in your browser
2. Set the path to your Calibre library's `metadata.db`
3. Create an admin user
4. Go to **Admin → Edit Basic Configuration → Feature Configuration**
5. Enable: **✅ Enable OPDS Catalog**
6. Enable: **✅ Allow anonymous browsing** (optional — for easier KOReader setup)
7. Save

---

## Finding Your Server's IP

```bash
# Linux/macOS
ip addr show | grep inet
# or
hostname -I

# Windows
ipconfig
```

Note the local IP (e.g., `192.168.1.100`). This is what you'll enter in KOReader.

---

## OPDS URL Format

```
http://YOUR_IP:8083/opds
```

Example: `http://192.168.1.100:8083/opds`

---

## Connecting KOReader

See the OPDS setup section in your device guide (e.g., [Kindle 4 → Step 7](../devices/kindle-4/README.md#step-7-configure-calibre-web-opds-in-koreader)).

The config file on your Kindle lives at:
```
/mnt/us/koreader/settings/opds.lua
```

---

## Tips

- **Book formats:** Calibre-Web can serve and convert between formats. Ensure EPUB and MOBI are available for best KOReader compatibility.
- **Adding books:** Use the Calibre desktop app to manage your library, or Calibre-Web's web upload.
- **Security:** For home use, no-auth OPDS is fine. If accessible from the internet, enable authentication.

---

## Resources

- [Calibre-Web GitHub](https://github.com/janeczku/calibre-web)
- [LinuxServer Calibre-Web Docker](https://docs.linuxserver.io/images/docker-calibre-web)
- [Calibre (desktop)](https://calibre-ebook.com/)

---

*See also: [KOReader Setup](../koreader/README.md)*
