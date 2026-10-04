Second code-signed Windows build — and first macOS package — of **Virtual SFX Lab** — Module 1: Wave Studio (Explo X2 Wave Flame pocket reference and virtual rehearsal). Carries the **V0.31c** studio.

## Download
- `Virtual-SFX-Lab-Windows-0.31.1-x64.zip` — unzip anywhere and run `Virtual SFX Lab.exe`. No installer, no admin rights. Replaces 0.31: unzip over the old folder or delete it; your layouts and settings live in `%LOCALAPPDATA%\WaveStudio` and are kept.
- `Virtual-SFX-Lab-macOS-0.31.1.zip` — readable Python source package for one Mac (receiver + full studio + First Guide). Unzip, then double-click `Virtual SFX Lab.command`. Needs **Python 3.10+ from python.org**; no pip packages. It is not a signed or notarized `.app`: the first launch of the `.command` file may need right-click → Open (or System Settings → Privacy & Security → Open Anyway). `START-HERE.md` inside explains the modes.
- `SHA256SUMS.txt` — checksums for both zips.

`Virtual SFX Lab.exe` is signed with Azure Artifact Signing (publisher **Rory Jones**, timestamped) with the same identity as 0.31. Right-click → Properties → Digital Signatures to inspect it. Windows SmartScreen may still show a reputation prompt on a new publisher identity for a while; choose **More info → Run anyway** if you trust the download.

## What's new in 0.31.1 (studio V0.31c)
- **Vista 3 Explo Layout show file**: a ready-made Vista 3 show (`.v3s`, 0.6 MB) with the Explo X2 Wave Flame fixtures patched to match the Wave Studio layout ships inside the app. A **Vista 3 Layout File** button sits beside **Vista / Receiver Settings** in the toolbar; the Vista 3 receiver setup dialog links the same file. Open it in Vista 3 (File → Open), match the sACN universes to the receiver, and Vista cues drive the flamers.
- **Phone / narrow-window Layout Controls**: the layout buttons are two even rows — Save, Load, Default and Reset Layout; then Export For Vista 3, Session Files, Autosave and Recordings.
- **Purchases open on the hosted site**: full studio, Windows app and macOS app at CAD $29.99 one-time (plus tax, price subject to change while updates continue) with a 14-day full refund. Tester codes shared personally by the developer unlock the studio free until 1.0. Nothing changes for this download — testers keep using it as before.
- Launcher 0.31.1; receiver unchanged (0.31.0). Credits counter and development log updated.

## Feedback
- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes.
- **[Bug report / idea on GitHub Issues](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads/issues/new/choose)** — attach screenshots and the log (`%LOCALAPPDATA%\WaveStudio\receiver.log`).

See the [README](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads#feedback) for what to test first and what to include. Please quote the build as `0.31.1 Windows` or `0.31.1 macOS`.

## Requirements
Windows 10/11 x64, or macOS 12+ with Python 3.10+ and a current browser (Safari, Chrome or Edge). For live sACN / Art-Net input, a lighting console or Vista 3 on the same network; the app also works standalone with no receiver.
