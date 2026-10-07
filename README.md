# Virtual SFX Lab — Downloads

Tester builds of **Virtual SFX Lab** (Module 1: Wave Studio — Explo X2 Wave Flame pocket reference and virtual rehearsal).

This repository holds only release downloads; there is no source code here.

## Latest: 0.33.0 for Windows and macOS (studio V0.33b, MA panel and receiver console presets)

Go to **[Releases](../../releases/latest)** and download `Virtual-SFX-Lab-Windows-0.33.0-x64.zip`. Updating from any 0.31 build: unzip over the old folder (or delete it); layouts and settings in `%LOCALAPPDATA%\WaveStudio` are kept.

1. Unzip anywhere (Desktop is fine). No installer, no admin rights.
2. Run `Virtual SFX Lab.exe`.
3. Pick **Start receiver + open studio** if you have a lighting console or Vista 3 sending sACN / Art‑Net on the network, or **Skip for now** to explore the studio standalone.

The app opens on the demo page; the First Guide manual opens automatically the first time you enter the full studio.

### macOS

Download `Virtual-SFX-Lab-macOS-0.33.0.zip` from the same release. It is a readable Python source package, not a signed `.app`.

1. Install **Python 3.10 or newer** from [python.org](https://www.python.org/downloads/macos/) if you do not have it (the universal2 installer). No pip packages are needed.
2. Unzip, then double-click `Virtual SFX Lab.command`. If macOS says it cannot be opened, right-click → **Open** once (or System Settings → Privacy & Security → **Open Anyway**).
3. The launcher starts the receiver (same-computer Vista / sACN preselected) and opens the studio in your browser. `Virtual SFX Lab — Preview Only.command` opens the studio without a receiver.

`START-HERE.md` inside the zip explains the modes and the network-interface choice. Vista interoperability on macOS is still pending native testing.

### About the Windows warning

`Virtual SFX Lab.exe` is code-signed (publisher **Rory Jones**, Azure Artifact Signing, timestamped). Right-click the exe → **Properties → Digital Signatures** to inspect it.

Because the publisher identity is new, Windows SmartScreen may still show "Windows protected your PC" for a while. Choose **More info → Run anyway**. This is a reputation prompt, not a signature failure; it goes away as more people run the app. Please do not disable your antivirus.

### Verify the download

`SHA256SUMS.txt` is attached to each release. On Windows:

```powershell
Get-FileHash .\Virtual-SFX-Lab-Windows-0.33.0-x64.zip -Algorithm SHA256
```

The hash must match the value in `SHA256SUMS.txt`.

## Also online (no download)

The hosted studio at [wavestudio.pplx.app](https://wavestudio.pplx.app/welcome.html) carries the newer web build (V0.34). Besides Wave Studio it now offers:

- **[Spark Studio](https://wavestudio.pplx.app/spark/index.html)** — the learning edition for early teens and classrooms: six virtual flames, faders, cues and GO, DMX addresses and universes, music timing, missions with XP, Classroom mode. Runs in the browser; nothing to install.
- **[Meet Pyro Pete](https://wavestudio.pplx.app/pete/index.html)** — the tutorial guide who lives in Wave Studio and Spark Studio. He peeks over the studio footer; click him and he jumps out. Press his settings for size, voice, mood, gravity, a talk-to-Pete microphone and an optional connection to your own AI provider key. The page also offers the **Pyro Pete browser extension** (0.3.1 developer preview, unpacked install for Comet, Chrome, Edge and Brave) that puts him on any web page.
- **[VSL Info Mode](https://wavestudio.pplx.app/vsl/index.html)** — the point-and-explain browser extension and Android preview.

These are hosted-only developer previews; they are not part of the desktop zips above.

## Requirements

Windows 10 or 11, 64‑bit; or macOS 12 or newer with Python 3.10+ and a current browser. A lighting console or Vista 3 on the same network is only needed for live input.

## Feedback

Two ways, use whichever is easier:

- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes. Best for your overall impressions after a session.
- **[GitHub Issues](../../issues/new/choose)** — pick **Bug report** or **Feedback / idea**. Needs a free GitHub account, but lets you attach screenshots and the log directly and follow the fix.

Either way, the details below are what make a report useful.

### What to test first

Spend 20–30 minutes on these before anything else; they are the parts most likely to differ between machines.

1. **Install and first run** — unzip, run `Virtual SFX Lab.exe`, note any Windows or antivirus prompts (screenshot them, including the exact wording).
2. **Launcher window** — is everything visible without dragging or scrolling, at your normal display scaling? Try both buttons.
3. **Demo page → full studio** — does the First Guide open on first entry? Can you find your way around using only the guide?
4. **Virtual stage** — build a short flame sequence, play it back, record a clip. Does the clip play, and does it carry the "Made with WaveStudio" watermark?
5. **Live input (if you have a console or Vista 3)** — Start receiver, pick your network adapter, send sACN or Art‑Net. Does the fixture respond? Any lag or dropped frames?
6. **Layouts** — rearrange panels, close and reopen the app. Did your layout survive?

Then use it the way you actually would on a show, and tell us where it fought you.

### What to include in every report

- Build: `0.33.0 Windows` or `0.33.0 macOS` (from the launcher title or the release you downloaded).
- Windows version and display scaling (Settings → System → Display → Scale), plus screen resolution.
- What you did, step by step, what you expected, and what happened instead.
- Screenshots or a short screen recording. For the stage itself, the studio's built‑in recording is ideal.
- For live-input problems: console or software name, protocol (sACN / Art‑Net), universe numbers, and whether the PC is on Wi‑Fi or Ethernet.
- The log file: `%LOCALAPPDATA%\WaveStudio\receiver.log` on Windows (paste the path into File Explorer's address bar); on macOS, copy the text from the Terminal window the `.command` opened. Attach it or paste the last 50 lines. It contains no personal data beyond local IP addresses.

### Severity, in your words

Tell us which of these it is so we can sort quickly:

- **Blocker** — can't install, launch, or get into the studio.
- **Wrong** — something behaves incorrectly or loses work.
- **Rough** — it works but is confusing, slow, or ugly.
- **Idea** — something you wish it did.

### Things we already know about

- SmartScreen "Windows protected your PC" on first run (new publisher identity; see above).
- Vista 3 show/profile export is a CSV / manual-build preview, not a native show file.
- Storefront purchases are not open; the Windows app is not time-limited for testers.
- Everything is stored locally and unencrypted; recording-share features expose your IP address to the other participant (WebRTC). Use a private network for tests.

## Terms

Tester builds are provided for evaluation only and may not be redistributed. © 2026 Rory Jones. All rights reserved.
