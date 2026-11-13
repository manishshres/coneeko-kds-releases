# Coneeko Kitchen Display

A kitchen display system for restaurants that run **Point of Success**. Orders rung
up at the till appear on kitchen screens within seconds, split by station the same
way the prep printers split them.

**[⬇ Download the latest version](https://github.com/manishshres/coneeko-kds-releases/releases/latest)**: `Coneeko-KDS-Setup.exe`

## Features

- **Stations by printer:** Tandoor, Curry and Expo, matching the POS prep printers.
- **Live order changes:** quantity changes, added dishes and new or edited notes
  update the ticket. Lines removed at the till are struck through.
- **Bump, priority, recall, print a chit,** and drag tickets into a different order.
- **Item tally:** how many of each dish are still open.
- **Per-screen settings:** text size, item list, 12- or 24-hour clock.
- **Warnings** when the till or the POS stops updating.
- **Auto-close** for forgotten tickets, and everything closes at the end of the night.
- **Works offline** on the local network. Read-only: it never changes the POS.
- **Updates itself** after hours.

## Install

1. Download **Coneeko-KDS-Setup.exe** from the
   [latest release](https://github.com/manishshres/coneeko-kds-releases/releases/latest)
   and run it on the till PC (Windows 10 or 11, 64-bit).
2. Choose **Install for me only**, so updates can install without an admin prompt.
3. In the Coneeko Kitchen Display app, set the **Restaurant name** and the
   **POS data folder** (usually `C:\Point of Success\Data`), then click **Save & apply**.
4. On each kitchen screen (tablet, TV or PC on the same network), open
   `http://<till-ip>:8787/kds` in a browser, full screen.

> Windows may show **"Windows protected your PC"** or **"Unknown publisher"**
> because the installer isn't code-signed yet. Click **More info → Run anyway**.

## Updates

The till checks this page daily, weekly or only when you click **Check now**
(set this in the app's Settings). A new version is downloaded and checked against
its `.sha256` checksum before it's used. It installs by itself after closing
time, and only when no tickets are open. Click **Install now** to install it
straight away. Kitchen screens reload on their own once the till is updated.

Every release includes `Coneeko-KDS-Setup.exe.sha256`. To check a download by hand
in PowerShell:

```powershell
Get-FileHash .\Coneeko-KDS-Setup.exe -Algorithm SHA256
```

## Support

contact@coneeko.com

---
This repository holds only the built installers. The source code is private.
