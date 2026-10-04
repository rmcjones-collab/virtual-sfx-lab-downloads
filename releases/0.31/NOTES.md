First code-signed Windows build of **Virtual SFX Lab** — Module 1: Wave Studio (Explo X2 Wave Flame pocket reference and virtual rehearsal).

## Download
- `Virtual-SFX-Lab-Windows-0.31-x64.zip` — unzip anywhere and run `Virtual SFX Lab.exe`. No installer, no admin rights.
- `SHA256SUMS.txt` — checksums for the zip.

`Virtual SFX Lab.exe` is signed with Azure Artifact Signing (publisher **Rory Jones**, timestamped). Right-click → Properties → Digital Signatures to inspect it. Windows SmartScreen may still show a reputation prompt on a new publisher identity for a while; choose **More info → Run anyway** if you trust the download.

## What's in 0.31
- Rebrand: Virtual SFX Lab, Module 1: Wave Studio. Opens on the free demo page; the full studio has a 7-day trial on the hosted site, CAD $29.99 one-time pricing shown (sales not yet open).
- Windows app: one-folder build bundling receiver 0.31.0 and the complete web app including the First Guide manual.
- Launcher: two actions — **Start receiver + open studio** (Enter) and **Skip for now — open studio without a receiver**. The window sizes itself to the screen and display scaling.
- Receiver 0.31.0: same-origin framing so the in-app manual works; demo page first.
- Studio: First Guide opens automatically on first open ("Open when the studio starts" toggle).

## Feedback
- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes.
- **[Bug report / idea on GitHub Issues](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads/issues/new/choose)** — attach screenshots and the log (`%LOCALAPPDATA%\WaveStudio\receiver.log`).

See the [README](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads#feedback) for what to test first and what to include.

## Requirements
Windows 10/11 x64. For live sACN / Art-Net input, a lighting console or Vista 3 on the same network; the app also works standalone with no receiver.
