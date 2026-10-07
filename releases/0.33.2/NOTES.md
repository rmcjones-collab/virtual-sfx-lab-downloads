Seventh code-signed Windows build of **Virtual SFX Lab** — Module 1: Wave Studio (Explo X2 Wave Flame pocket reference and virtual rehearsal). Carries the **V0.34** studio. The macOS launcher package stays at 0.33.0 and is included unchanged.

## Download
- `Virtual-SFX-Lab-Windows-0.33.2-x64.zip` — unzip anywhere and run `Virtual SFX Lab.exe`. No installer, no admin rights. Replaces 0.33.1, 0.33.0 and 0.31.x: unzip over the old folder or delete it; your layouts and settings live in `%LOCALAPPDATA%\WaveStudio` and are kept.
- `Virtual-SFX-Lab-macOS-0.33.0.zip` — readable Python source package for one Mac (receiver + full studio + First Guide), unchanged from 0.33.0. Unzip, then double-click `Virtual SFX Lab.command`. Needs **Python 3.10+ from python.org**; no pip packages. Not a signed or notarized `.app`: the first launch may need right-click → Open (or System Settings → Privacy & Security → Open Anyway).
- `SHA256SUMS.txt` — checksums for both zips.

`Virtual SFX Lab.exe` is signed with Azure Artifact Signing (publisher **Rory Jones**, timestamped) with the same identity as the 0.31, 0.33.0 and 0.33.1 builds. Right-click → Properties → Digital Signatures to inspect it. Windows SmartScreen and antivirus reputation systems may prompt on a brand-new file for a while; choose **More info → Run anyway** only if you downloaded it from here or from virtualsfxlab.com, and never disable your antivirus for it.

## What's new in 0.33.2 (Windows)
- **Fix: the launcher no longer closes itself when minimized to the system tray.** In 0.33.1 the first tray event (minimizing, or hovering the tray icon) ended the process (Windows recorded exception 0xc0000409). The tray code now queues events and lets the window's own timer deliver them. Verified against the released exe on a Windows test machine before and after the fix.
- `crash.log` beside `receiver.log` records the Python stack if the launcher ever crashes hard, so a report can include it.
- The bundled welcome page shows the correct build number.

## What's new since 0.33.0 (shipped in 0.33.1)
- **System tray**: the Virtual SFX Lab window minimizes to the tray (Minimize to tray button or the window's minimize button). Hovering the tray icon shows state, protocol, interface, universes, DMX packet count and rate, rejected and source-conflict counts and the studio address. Left click reopens the window; right click offers Open window, Open studio, Start or Stop receiver, Open log folder and Exit.
- **Virtual SFX Lab logo** as the exe, window and tray icon; the header reads "Virtual SFX Lab 0.33.2".
- **Receiver reliability**: the receive loops survive Windows socket errors (an oversized datagram, or the reset Windows reports after a discovery reply to a closed port); errors are counted in the status line instead of silently stopping reception. sACN joins every active network adapter and the log lists each join, so a console on a second adapter is heard without choosing an interface. Universes you did not select are filtered for Art-Net as well as sACN.
- **Launcher**: a failure inside the status refresh no longer freezes the counters; if `%LOCALAPPDATA%\WaveStudio` cannot be written, the log and settings fall back to the temp folder with a warning instead of a silent exit.
- **Vista Check** (`tools\vista_check.py`, `Run-Vista-Check.cmd`): separate messages for an address that is not on this PC, a port in use and a failed multicast join; the report lists the multicast groups joined per adapter; grandMA2 Draft sACN counts as DMX.
- **Offline pages**: the Pete page and Spark Studio ship in the package; links into the VSL Info Mode download folder open virtualsfxlab.com instead of a 404.
- Studio **V0.34** web code: VSL Info Mode downloads, Pete settings tabs, Spark Studio, the MA panel under Layout Controls, and the brand refresh.

## Feedback
- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes.
- **[Bug report / idea on GitHub Issues](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads/issues/new/choose)** — attach screenshots and the log (`%LOCALAPPDATA%\WaveStudio\receiver.log`).
- **[Discord](https://discord.gg/tukmpvS8T5)** — the beta-tester community.

Please quote the build as `0.33.2 Windows` or `0.33.0 macOS`. If you run two network adapters, tell us whether the launcher log shows one sACN join per adapter and whether a "Receive errors" line ever appears.

## Requirements
Windows 10/11 x64, or macOS 12+ with Python 3.10+ and a current browser (Safari, Chrome or Edge). For live sACN / Art-Net input, a lighting console (grandMA3, grandMA2, Vista 3 or any sACN / Art-Net source) on the same network; the app also works standalone with no receiver.
