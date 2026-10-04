# Virtual SFX Lab — Downloads

Tester builds of **Virtual SFX Lab** (Module 1: Wave Studio — Explo X2 Wave Flame pocket reference and virtual rehearsal).

This repository holds only release downloads; there is no source code here.

## Latest: 0.31 for Windows

Go to **[Releases](../../releases/latest)** and download `Virtual-SFX-Lab-Windows-0.31-x64.zip`.

1. Unzip anywhere (Desktop is fine). No installer, no admin rights.
2. Run `Virtual SFX Lab.exe`.
3. Pick **Start receiver + open studio** if you have a lighting console or Vista 3 sending sACN / Art‑Net on the network, or **Skip for now** to explore the studio standalone.

The app opens on the demo page; the First Guide manual opens automatically the first time you enter the full studio.

### About the Windows warning

`Virtual SFX Lab.exe` is code-signed (publisher **Rory Jones**, Azure Artifact Signing, timestamped). Right-click the exe → **Properties → Digital Signatures** to inspect it.

Because the publisher identity is new, Windows SmartScreen may still show "Windows protected your PC" for a while. Choose **More info → Run anyway**. This is a reputation prompt, not a signature failure; it goes away as more people run the app. Please do not disable your antivirus.

### Verify the download

`SHA256SUMS.txt` is attached to each release. On Windows:

```powershell
Get-FileHash .\Virtual-SFX-Lab-Windows-0.31-x64.zip -Algorithm SHA256
```

The hash must match the value in `SHA256SUMS.txt`.

## Requirements

Windows 10 or 11, 64‑bit. A lighting console or Vista 3 on the same network is only needed for live input.

## Feedback

Send notes, screenshots and recordings to the address you were given with your invite. Tester builds are pre-release: everything is stored locally and unencrypted on your machine, and the studio's recording-share features expose your IP address to the other participant (WebRTC).

## Terms

Tester builds are provided for evaluation only and may not be redistributed. © 2026 Rory Jones. All rights reserved.
