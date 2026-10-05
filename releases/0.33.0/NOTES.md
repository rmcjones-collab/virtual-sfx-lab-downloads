Fifth code-signed Windows build and fourth macOS package of **Virtual SFX Lab** — Module 1: Wave Studio (Explo X2 Wave Flame pocket reference and virtual rehearsal). Carries the **V0.33b** studio with grandMA2 / grandMA3 support.

## Download
- `Virtual-SFX-Lab-Windows-0.33.0-x64.zip` — unzip anywhere and run `Virtual SFX Lab.exe`. No installer, no admin rights. Replaces 0.31.x: unzip over the old folder or delete it; your layouts and settings live in `%LOCALAPPDATA%\WaveStudio` and are kept.
- `Virtual-SFX-Lab-macOS-0.33.0.zip` — readable Python source package for one Mac (receiver + full studio + First Guide). Unzip, then double-click `Virtual SFX Lab.command`. Needs **Python 3.10+ from python.org**; no pip packages. It is not a signed or notarized `.app`: the first launch of the `.command` file may need right-click → Open (or System Settings → Privacy & Security → Open Anyway). `START-HERE.md` inside explains the modes.
- `SHA256SUMS.txt` — checksums for both zips.

`Virtual SFX Lab.exe` is signed with Azure Artifact Signing (publisher **Rory Jones**, timestamped) with the same identity as the 0.31 builds. Right-click → Properties → Digital Signatures to inspect it. Windows SmartScreen may still show a reputation prompt on a new publisher identity for a while; choose **More info → Run anyway** if you trust the download.

## What's new in 0.33.0 (studio V0.33b, MA panel and receiver console presets)
- **Receiver console presets**: the Virtual SFX Lab window has a **Console** drop-down (Vista 3, grandMA3 console / onPC, grandMA2 console / onPC, Other sACN / Art-Net source) above Input mode. It sets the console-specific output hints and the status line ("Listening — waiting for grandMA3"), and the studio's **Vista & MA Receiver** dialog opens on that console's tab with a summary of the running receiver. The macOS launcher shows the same choice as a numbered menu (sACN / Art-Net from Vista 3, sACN from grandMA3, sACN from grandMA2, Art-Net from a grandMA, other).
- **Receiver 0.33.0**: reads sACN in the ratified E1.31 Final layout **and** the older Draft layout grandMA2 still offers (counted separately), accepts unicast as well as multicast sACN (grandMA3 Unicast mode) and ignores Art-Net ArtSync. Still receive-only — nothing is transmitted to the console.
- **MA panel** (studio V0.33): a grandMA2 / grandMA3 command section under the Cue Stack — X1–X10, Go+, Go−, Pause, Off, Store, Update, Fixture, Group, Preset, Cue, Exec, Thru, At, the number pad, Please and the rest. Keys use MA grammar (`Fixture 1 Thru 4 At 30 Please` parks four heads at 30°, `Store Cue` records the selection, `Exec 5 At 60` sets fader 5, Go+ runs the Cue Stack) and can be typed on the command line. A physical grandMA presses them through the sACN control universe: **Physical grandMA console → Patch Keys In Order** (channels 101–184), one dimmer per key on the desk on Temp executor buttons; `06-ma-keys.csv` in Export For grandMA lists every key and channel. Learn, If, Set, View and Effect report that they are not modelled.
- The receiver button is now **Vista & MA Receiver**; First Guide Part 5 gains §5.7 (MA panel) and the receiver console presets table, plus troubleshooting rows. Also carries the V0.32 grandMA export and live-input instructions, which never shipped as a desktop build.

## Feedback
- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes.
- **[Bug report / idea on GitHub Issues](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads/issues/new/choose)** — attach screenshots and the log (`%LOCALAPPDATA%\WaveStudio\receiver.log`).
- **[Discord](https://discord.gg/tukmpvS8T5)** — the beta-tester community.

See the [README](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads#feedback) for what to test first and what to include. Please quote the build as `0.33.0 Windows` or `0.33.0 macOS`. grandMA testers: tell us which console / onPC version you imported the GDTF, MVR or XML into and whether the fixture type, patch and positions arrived intact.

## Requirements
Windows 10/11 x64, or macOS 12+ with Python 3.10+ and a current browser (Safari, Chrome or Edge). For live sACN / Art-Net input, a lighting console (grandMA3, grandMA2, Vista 3 or any sACN / Art-Net source) on the same network; the app also works standalone with no receiver.
