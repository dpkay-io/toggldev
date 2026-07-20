<h1 align="center">TogglDev — One Tap. Developer Mode.</h1>

<p align="center">
  Toggle Android Developer Options on and off instantly — via widget, tile, shortcut, or remotely from your desktop.<br>
  Your settings are automatically saved and restored. No root required.
</p>

<p align="center">
  <a href="https://github.com/dpkay-io/toggldev/releases"><img src="https://img.shields.io/github/downloads/dpkay-io/toggldev/total?style=for-the-badge&color=3ddc84&label=GitHub%20Downloads" alt="GitHub Downloads"></a>
  &nbsp;
  <a href="https://github.com/dpkay-io/toggldev/stargazers"><img src="https://img.shields.io/github/stars/dpkay-io/toggldev?style=for-the-badge&color=3ddc84" alt="GitHub Stars"></a>
  &nbsp;
  <a href="https://github.com/dpkay-io/toggldev"><img src="https://img.shields.io/badge/⭐_Star_This_Repo-black?style=for-the-badge&logo=github&logoColor=white" alt="Star This Repo"></a>
</p>

<p align="center">
  <a href="https://github.com/dpkay-io/toggldev/releases/latest"><img src="screens/badge_github.svg" alt="Download APK from GitHub" height="80"></a>
  &nbsp;&nbsp;
  <a href="https://play.google.com/store/apps/details?id=com.dpkay.apps.developer_options_toggler"><img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play" height="80"></a>
</p>

---

## The Problem

You enable Developer Options for faster animations, USB debugging, and app testing. Then your **banking app detects it and locks you out**. So you disable everything, use the bank, re-enable, and reconfigure every setting. Again and again.

**TogglDev ends this cycle.** One tap off, one tap back on — every setting automatically saved and restored.

---

## Snapshots

<p align="center">
  <img src="screens/1.png" alt="TogglDev — One Tap Developer Mode" width="270">
  &nbsp;&nbsp;&nbsp;
  <img src="screens/2.png" alt="TogglDev App Interface" width="270">
</p>

---

## Features

### One-Tap Toggles
- **Developer Options** — master on/off with settings snapshot & restore
- **USB Debugging** (ADB)
- **Wireless Debugging** (ADB over WiFi) — shows IP:Port, tap to copy
- **Animation Scales** — window, transition, animator duration (0x–2x)
- **Show Touches**, **Pointer Location**, **Show Layout Bounds**
- **Stay Awake While Plugged In**, **Force RTL Layout**, **Don't Keep Activities**, **Wait for Debugger**
- **Wi-Fi Scan Throttling**, **Bluetooth Disable Absolute Volume**, **Mobile Data Always On**, **Freeform Windows**
- **Modify all supported settings inline** — change values directly from within the app

### Toggle From Anywhere

| Method | What You Get |
|--------|-------------|
| **Quick Settings Tiles** | 6 tiles in your notification shade — swipe down, tap, done |
| **Home Screen Widgets** | 7 widgets with real-time status — including Remote Access |
| **App Shortcuts** | Long-press icon → Turn On / Turn Off / Toggle / Dev Settings |
| **Automation** | Tasker, IFTTT, MacroDroid — control via intents |

### Remote Access
Control your device's developer settings from your desktop — no cable needed. TogglDev runs a lightweight HTTP server on your phone with secure pairing (6-digit code + token auth). Toggle any setting, check status, or grab wireless debug info from your computer.

- **Companion app:** [TogglDev Remote](https://github.com/dpkay-io/toggldev-remote) — a desktop client for seamless remote control
- **Home screen widget** shows server status, IP:port, and pairing code at a glance
- **Free tier:** 10 minutes/day — unlimited for Gourmet supporters

### Command Automation
Define custom ADB/shell commands that run automatically when you toggle Developer Options, USB Debugging, or WiFi Debugging on/off. Separate commands for each trigger event, execution logs with timestamps and exit codes, and automatic privilege detection (base, ADB-elevated, or root).

### App Rules
Create rules that apply settings to groups of apps. Force-enable, force-disable, or run custom actions when specific apps launch. Conflict detection warns if multiple rules target the same app. Free tier includes 2 rules — unlimited for supporters.

### Banking App Shield
Automatically turn off Developer Options when banking or payment apps launch. Configurable re-enable delay (30s to 5 minutes, or never). Uses an accessibility service that only reads the foreground app name — nothing else.

### Accessibility Hide
Some banking and security apps detect not just Developer Options, but also running accessibility services. Accessibility Hide temporarily disables all accessibility services when a targeted app launches, then silently restores them when the app exits. Works per-app — select which apps trigger the hide. Requires Usage Access permission for app lifecycle monitoring. Integrates with App Rules so your existing rules get accessibility hiding automatically.

### Smart Snapshot & Restore
When you disable Developer Options, TogglDev saves every setting. When you re-enable, everything is restored exactly as it was.

### Themes
Choose your preferred app theme to match your style or system settings.

### Multi-Language
Supports 18 languages: Arabic, Chinese, Danish, Dutch, English, French, German, Greek, Indonesian, Japanese, Korean, Persian, Polish, Portuguese (BR), Russian, Spanish, Thai, and Turkish.

---

## Privacy & Trust

| | |
|---|---|
| **100% Private** | No personal data collected. Everything stays on your device. |
| **100% Ad-Free** | No ads. Ever. |
| **No Tracking** | No analytics. No monitoring. Period. |
| **Works Offline** | No internet required. Works completely offline. |
| **Safe & Verified** | Google Play Protect verified. Open APK on GitHub. |

---

## Specs

| | |
|---|---|
| **Size** | ~2.7 MB |
| **Languages** | 18 |
| **Android** | 8.0+ (Oreo) |
| **GMS** | Not required — works on any Android device |

---

## Install

### Google Play (Recommended)

<a href="https://play.google.com/store/apps/details?id=com.dpkay.apps.developer_options_toggler"><img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play" height="80"></a>

### APK from GitHub

1. Download **[TogglDev.apk](https://github.com/dpkay-io/toggldev/releases/latest)** from the latest release
2. Transfer to your device or download directly on it
3. Tap the APK and follow install prompts (enable "Install from unknown sources" if prompted)
4. Open the app and follow the onboarding setup

### Required Permission

TogglDev needs `WRITE_SECURE_SETTINGS` to toggle developer options. One-time ADB command:

```
adb shell pm grant com.dpkay.apps.developer_options_toggler android.permission.WRITE_SECURE_SETTINGS
```

The app's onboarding screen walks you through this.

> **Note for OnePlus/Xiaomi users:** You might have to **Disable Permission Monitoring** or **Disable System Optimization** in your developer options for the ADB command to work.

---

## Roadmap

- [x] Theme support
- [x] One tap Wireless debugging widget
- [x] App rules to customize individual developer setting toggle for app launch
- [x] Command automation to run any shell commands on toggle of Developer options and Debugging
- [x] Remote access and MCP to seamlessly control Developer options for Agentic development with Claude, Gemini and others
- [ ] Shizuku integrations
- [x] Accessibility Hide — auto-disable accessibility services for targeted apps
- [ ] Remove Accessibility Services dependency
- [ ] Master widget to support more toggles
- [ ] App commands automation

---

## Featured In

- [**HowToMen**](https://youtu.be/2QBFRcqee7I?t=622) — Top 15 Best Android Apps, July 2026
- [**ODORIZZI**](https://youtu.be/RaAqTCALHpU) — Nunca mais desligue o MODO DESENVOLVEDOR no Android
- [**Trakin Tech Tamil**](https://youtu.be/1RoaZy-zVHA?si=A7Nj5sonPxcDfzNj&t=134) — Best New Free Android Apps

---

## Links

- [Website](https://dpkay.com/toggldev)
- [Google Play Store](https://play.google.com/store/apps/details?id=com.dpkay.apps.developer_options_toggler)
- [TogglDev Remote (Companion App)](https://github.com/dpkay-io/toggldev-remote)
- [Privacy Policy](https://dpkay.com/toggldev/privacy-policy.html)
---
