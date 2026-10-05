Fourth code-signed Windows build and third macOS package of **Virtual SFX Lab** — Module 1: Wave Studio (Explo X2 Wave Flame pocket reference and virtual rehearsal). Carries the **V0.32** studio with grandMA2 / grandMA3 support.

## Download
- `Virtual-SFX-Lab-Windows-0.32.0-x64.zip` — unzip anywhere and run `Virtual SFX Lab.exe`. No installer, no admin rights. Replaces 0.31.x: unzip over the old folder or delete it; your layouts and settings live in `%LOCALAPPDATA%\WaveStudio` and are kept.
- `Virtual-SFX-Lab-macOS-0.32.0.zip` — readable Python source package for one Mac (receiver + full studio + First Guide). Unzip, then double-click `Virtual SFX Lab.command`. Needs **Python 3.10+ from python.org**; no pip packages. It is not a signed or notarized `.app`: the first launch of the `.command` file may need right-click → Open (or System Settings → Privacy & Security → Open Anyway). `START-HERE.md` inside explains the modes.
- `SHA256SUMS.txt` — checksums for both zips.

`Virtual SFX Lab.exe` is signed with Azure Artifact Signing (publisher **Rory Jones**, timestamped) with the same identity as the 0.31 builds. Right-click → Properties → Digital Signatures to inspect it. Windows SmartScreen may still show a reputation prompt on a new publisher identity for a while; choose **More info → Run anyway** if you trust the download.

## What's new in 0.32.0 (studio V0.32, grandMA2 / grandMA3 update)
- **grandMA3 and grandMA2 live input**: the receiver already speaks standard sACN (E1.31) and Art-Net, so MA consoles — or onPC with MA hardware attached — drive the virtual units like Vista. **Vista / Receiver Settings** now has Vista 3, grandMA3 and grandMA2 tabs with the console-side output steps (DMX Protocols → sACN / Art-Net on grandMA3; Setup → Network Protocols on grandMA2), universe numbering (sACN universe 1 = Art-Net port address 0 = Wave Studio slot 0) and MA's onPC hardware rule. `START-HERE` and the setup guide carry the same settings.
- **Export For grandMA** (Layout Controls, next to Export For Vista 3): a ZIP with a **GDTF** fixture type for the Explo X2 Wave Flame (Tilt, Speed, Ignition, Open Time, Program with a named channel set for every sequence, Arm), an **MVR** scene for grandMA3 with absolute addresses, stage positions and mount rotations (Menu → Show Creator → Partial Show Read → MVR), a **grandMA2 fixture-type XML** and **fixture-layer XML** (`Import "wavestudio_layer" At Layer 1`), and CSV sheets for patch, cues, cuelists, cue contents (DMX and %) and fader assignments. GDTF and MVR are validated against the official DIN SPEC 15800 / 15801 schemas; the grandMA2 XML follows the structure of grandMA2 3.4 exports and should be verified in onPC. MA show files are not a documented format, so cue contents are programmed on the console from sheet 04. **GDTF Only** saves just the fixture type.
- **First Guide Part 5.6**: grandMA2 / grandMA3 live input and export, with troubleshooting rows and MA documentation links; Control Info and the written tutorials cover the new button.
- Launcher 0.32.0; receiver unchanged (0.31.0).

## Feedback
- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes.
- **[Bug report / idea on GitHub Issues](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads/issues/new/choose)** — attach screenshots and the log (`%LOCALAPPDATA%\WaveStudio\receiver.log`).
- **[Discord](https://discord.gg/tukmpvS8T5)** — the beta-tester community.

See the [README](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads#feedback) for what to test first and what to include. Please quote the build as `0.32.0 Windows` or `0.32.0 macOS`. grandMA testers: tell us which console / onPC version you imported the GDTF, MVR or XML into and whether the fixture type, patch and positions arrived intact.

## Requirements
Windows 10/11 x64, or macOS 12+ with Python 3.10+ and a current browser (Safari, Chrome or Edge). For live sACN / Art-Net input, a lighting console (grandMA3, grandMA2, Vista 3 or any sACN / Art-Net source) on the same network; the app also works standalone with no receiver.
