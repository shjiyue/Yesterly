<p align="right">
  <a href="./README.md"><img alt="English" src="https://img.shields.io/badge/lang-English-blue?style=for-the-badge"></a>
  <a href="./README.zh-CN.md"><img alt="简体中文" src="https://img.shields.io/badge/lang-简体中文-lightgrey?style=for-the-badge"></a>
</p>

# Yesterly

**Focus on your work—recap from what you actually did.**

Yesterly is an AI work-memory and recap app for **macOS** and **Windows**. Keep working as usual; it captures on-screen context on your schedule, turns fragments into a **local timeline**, and helps you draft daily, weekly, monthly, yearly, or custom recaps from real entries—not from memory alone.

The product does two things: **capture your work** and **turn entries into recaps**. Instead of asking “what did I do today?” at midnight, you review the timeline, fix the material, then export something you can actually use.

> This repository is the **official release channel** for Yesterly installers, release notes, and product help. It does **not** contain product source code.

[Product site](https://jijianribao.qitingai.com) · [Download latest](https://github.com/shjiyue/Yesterly/releases/latest) · [All releases](https://github.com/shjiyue/Yesterly/releases) · [Plans & pricing](https://jijianribao.qitingai.com/pricing) · [Privacy](https://jijianribao.qitingai.com/privacy)

## Download & install

Current release: **v0.1.5**.

| Platform | Device | Installer |
| --- | --- | --- |
| macOS Apple Silicon / ARM64 | Mac with Apple M series | [Download DMG](https://github.com/shjiyue/Yesterly/releases/download/v0.1.5/yesterly-0.1.5-mac-arm64.dmg) |
| macOS Intel / x64 | Mac with Intel CPU | [Download DMG](https://github.com/shjiyue/Yesterly/releases/download/v0.1.5/yesterly-0.1.5-mac-x64.dmg) |
| Windows x64 | 64-bit Windows PC | [Download EXE](https://github.com/shjiyue/Yesterly/releases/download/v0.1.5/yesterly-0.1.5-win-x64-setup.exe) |

Not sure which Mac chip you have? Apple menu → **About This Mac** → **Chip** or **Processor**. Pick the matching installer.

### macOS

1. Download the `.dmg` for your chip and open it.
2. Drag **Yesterly** into **Applications**, then launch from Applications.
3. When prompted, allow **Screen Recording** in System Settings.
4. If you use Enter-to-capture, grant Accessibility (and any other permissions the app requests); restart the app if macOS asks you to.

### Windows

1. Download the `.exe` installer.
2. Run the setup wizard.
3. Launch Yesterly and complete sign-in, model setup, and capture preferences.

Installers live under each Release **Assets**. GitHub’s auto **Source code (zip/tar.gz)** is only a snapshot of this docs repo—not the desktop app and not product source.

## What Yesterly does

### 1. Capture work as you go

- **Scheduled capture** at your chosen interval.
- **Enter key** (optional): trigger capture; rapid triggers merge.
- **Custom hotkeys** for important moments.
- **Multi-monitor** selection.
- **Dedup & idle skip**: skip automatic rounds when the pointer stays idle; manual hotkeys still work.
- **Start / pause** recording when you need to.

Summaries come from what’s visible on screen and the frontmost window. Enter listening triggers capture only—it does not log keystrokes—but anything on screen may appear in a capture.

### 2. Review and edit on a local timeline

- Browse entries by date and time range.
- Read summaries, add notes, revise or delete entries.
- Stats and activity heat maps help you see patterns—not performance scores.

### 3. Generate recaps from your entries

- Daily, weekly, monthly, yearly, and custom recaps.
- Preview source material before generation.
- Built-in templates plus your own; export **TXT / Markdown** or copy to clipboard.

Always verify AI output—especially status, numbers, outcomes, and next steps.

### 4. Separate capture model and recap model

| Use case | Options | Notes |
| --- | --- | --- |
| Screen understanding | Yesterly subscription model, custom API, third-party OAuth models | Needs vision-capable models; test before enabling |
| Direct recap output | Custom API, third-party OAuth models | Configure under **Recap model** |
| Web recap flow | DeepSeek web | Attachments + prompts in the browser; save results locally |

**The subscription capture model is not used for direct recap output.** Configure a recap model or use the web flow. Third-party availability and quotas depend on each provider.

You can point custom models at compatible local endpoints; account, device auth, and subscription checks still require network access.

### 5. Screenshots & local backup

- By default, screenshots are temporary for recognition; text entries remain.
- Optional retention with day and disk limits.
- Encrypted local backup/restore for entries, recaps, templates, and optional screenshots—not login tokens or model OAuth (reconfigure after restore).

## First run

1. **Install & sign in** via the browser flow and desktop authorization.
2. **Check your plan** in the account area (details on the site and in-app).
3. **Grant capture permissions** (Screen Recording on macOS; Accessibility if using Enter capture).
4. **Choose a capture model** (subscription or custom / OAuth).
5. **Set capture options** (displays, interval, Enter / hotkeys).
6. **Work normally**, then review and fix the timeline.
7. **Generate recaps** with your template and output method; review before sharing.

The app tries to start capturing on launch after sign-in, entitlements, models, and permissions pass. Pause only applies for the current session—pause before sensitive content.

## Data & privacy

**Your work material stays on your device; you choose where models run.**

| Data / action | Handling |
| --- | --- |
| Summaries, timeline, recaps, edits | Stored on this device—no Yesterly cloud sync of work content |
| Screen recognition | Frames + prompts go to the model you chose (local model = local service) |
| Direct recap | Text material + template + instructions to your recap model |
| DeepSeek web flow | Attachments + prompts in DeepSeek web sessions |
| Account & billing | Sign-in, device auth, plans, orders, usage metadata in the cloud |

Local storage ≠ fully offline: cloud models receive your material; Yesterly does not proxy model traffic. See [Privacy on the site](https://jijianribao.qitingai.com/privacy) and in-app **Privacy**.

Signing in on another device does not sync an existing timeline—back up before switching machines.

## FAQ

### Is this open source?

No. This repo publishes product help and installers only—not application source.

### Nothing new appears after I start capturing?

Check sign-in, plan status, pause state, model availability, and Screen Recording permission. Idle skip or duplicate frames can skip a round. See **Preferences → App log** for details.

### Why can’t I generate a recap directly?

Capture and recap models are separate. Configure and test a recap model (custom API or OAuth) or use the DeepSeek web flow.

### Do I still need an account with my own model?

Yes. Device auth and entitlements apply even with BYO models.

### Fully offline?

Sign-in and subscription checks need the network. Local models can keep content on-machine, but the app is not fully offline.

### Upgrading?

Use **Preferences → Updates** or the [latest Release](https://github.com/shjiyue/Yesterly/releases/latest). Back up first.

### Feedback?

Use in-app support or [Issues](https://github.com/shjiyue/Yesterly/issues). Include OS, chip, app version, steps, and errors—redact secrets and sensitive work.

## About this repository

- **README**: product overview and download links ([English](./README.md) · [简体中文](./README.zh-CN.md)).
- **Releases**: installers, notes, and SHA-256 checksums.
- **Issues**: feedback and questions.

Installers are Release assets only—they are not checked into the Git tree. Product source is not published here.
