# Scripts

> Helper scripts for Kindle Revival workflows

---

## Overview

This folder contains (or will contain) helper scripts for common tasks:

- Batch-copying books to Kindle via SCP/rsync
- Verifying jailbreak status
- Backing up KOReader settings
- Automating Calibre-Web setup

---

## Current Scripts

*Coming soon — contributions welcome!*

---

## Contribute a Script

Have a script that made your Kindle Revival setup easier? Open a PR!

Guidelines:
- Works on Linux, macOS, and ideally Windows (WSL)
- Includes a usage comment at the top
- Does not hardcode IPs or paths — use variables

---

## Quick One-Liners

### Push all EPUBs to Kindle via SSH
```bash
find ~/Books -name "*.epub" -exec scp -P 2222 {} root@192.168.1.XXX:/mnt/us/documents/ \;
```

### rsync entire library to Kindle
```bash
rsync -avz --progress -e "ssh -p 2222" ~/Books/ root@192.168.1.XXX:/mnt/us/documents/
```

### Check if Kindle is reachable on network
```bash
ssh -p 2222 -o ConnectTimeout=5 root@192.168.1.XXX echo "Kindle reachable" 2>/dev/null || echo "Not reachable — is KOReader open?"
```
