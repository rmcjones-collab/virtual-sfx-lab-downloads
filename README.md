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

Please report through **[Issues](../../issues/new/choose)** in this repository; pick **Bug report** or **Feedback / idea**. You need a free GitHub account. If you'd rather not use GitHub, reply to the message that sent you here with the same details.

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

- Build: `0.31 Windows` (from the launcher title or the release you downloaded).
- Windows version and display scaling (Settings → System → Display → Scale), plus screen resolution.
- What you did, step by step, what you expected, and what happened instead.
- Screenshots or a short screen recording. For the stage itself, the studio's built‑in recording is ideal.
- For live-input problems: console or software name, protocol (sACN / Art‑Net), universe numbers, and whether the PC is on Wi‑Fi or Ethernet.
- The log file: `%LOCALAPPDATA%\WaveStudio\receiver.log` (paste the path into File Explorer's address bar). Attach it or paste the last 50 lines. It contains no personal data beyond local IP addresses.

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
