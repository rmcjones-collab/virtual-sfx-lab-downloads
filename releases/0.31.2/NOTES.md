Third code-signed Windows build and second macOS package of **Virtual SFX Lab** — Module 1: Wave Studio (Explo X2 Wave Flame pocket reference and virtual rehearsal). Carries the current **V0.31c** studio with the AI Assist update.

## Download
- `Virtual-SFX-Lab-Windows-0.31.2-x64.zip` — unzip anywhere and run `Virtual SFX Lab.exe`. No installer, no admin rights. Replaces 0.31.1: unzip over the old folder or delete it; your layouts and settings live in `%LOCALAPPDATA%\WaveStudio` and are kept.
- `Virtual-SFX-Lab-macOS-0.31.2.zip` — readable Python source package for one Mac (receiver + full studio + First Guide). Unzip, then double-click `Virtual SFX Lab.command`. Needs **Python 3.10+ from python.org**; no pip packages. It is not a signed or notarized `.app`: the first launch of the `.command` file may need right-click → Open (or System Settings → Privacy & Security → Open Anyway). `START-HERE.md` inside explains the modes.
- `SHA256SUMS.txt` — checksums for both zips.

`Virtual SFX Lab.exe` is signed with Azure Artifact Signing (publisher **Rory Jones**, timestamped) with the same identity as 0.31 and 0.31.1. Right-click → Properties → Digital Signatures to inspect it. Windows SmartScreen may still show a reputation prompt on a new publisher identity for a while; choose **More info → Run anyway** if you trust the download.

## What's new in 0.31.2 (studio V0.31c, AI Assist update)
- **AI Assist reads the manual**: questions and keyword searches now return matching First Guide sections alongside the tutorials, with **Open In Manual**, **Read Aloud** and **Search With Perplexity** buttons.
- **Information mode**: press **Ctrl + ?** (or the **?** button beside **Manual**) and hover any control for a plain-language explanation with links to its manual section and tutorial. Press again or Esc to leave.
- **Bring your own AI assistant**: connect Perplexity (recommended), OpenAI, Anthropic, Gemini or a custom endpoint in AI Assist → Your AI Assistant; the key stays in your browser and any fees are billed by that provider, outside Virtual SFX Lab. On the hosted site a built-in site assistant answers without set-up.
- **More human Read Aloud**: the app picks the most natural voice your device offers, speaks sentence by sentence and reads shortcuts and units cleanly; choose voice, pace and pitch under AI Assist → Read Aloud Voice & Narration. Studio narration (a cloud voice) is available on the hosted site or with your own OpenAI key; this offline package uses the device voice.
- **Checklists**: create, edit and delete your own checklists next to the built-in colleague test.
- **Layout**: rotation buttons (−5 / +5, [ and ]) can be added to any panel; Discord community links, beta-tester sign-up and an FAQ on the landing page.
- Launcher 0.31.2; receiver unchanged (0.31.0).

## Feedback
- **[Tester feedback form](https://docs.google.com/forms/d/e/1FAIpQLSd2nTsyXxWeg4TpHbVNckw4pIf5FeYQs_7vh1HtyQ04IXbB_w/viewform)** — no account needed, about five minutes.
- **[Bug report / idea on GitHub Issues](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads/issues/new/choose)** — attach screenshots and the log (`%LOCALAPPDATA%\WaveStudio\receiver.log`).
- **[Discord](https://discord.gg/tukmpvS8T5)** — the beta-tester community.

See the [README](https://github.com/rmcjones-collab/virtual-sfx-lab-downloads#feedback) for what to test first and what to include. Please quote the build as `0.31.2 Windows` or `0.31.2 macOS`.

## Requirements
Windows 10/11 x64, or macOS 12+ with Python 3.10+ and a current browser (Safari, Chrome or Edge). For live sACN / Art-Net input, a lighting console or Vista 3 on the same network; the app also works standalone with no receiver.
