# TogglDev — Developer Options Toggler

Toggle Android developer options on and off in one tap — no digging through Settings menus.

<a href="https://play.google.com/store/apps/details?id=com.dpkay.apps.developer_options_toggler"><img src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png" alt="Get it on Google Play" height="80"></a>

## Install from APK

1. Download **[TogglDev.apk](TogglDev.apk)** from this repository
2. Transfer it to your Android device (or download directly on the device)
3. Tap the APK file and follow the install prompts
   - You may need to enable **"Install from unknown sources"** for your browser or file manager
4. After installing, open the app and follow the onboarding setup

### Required permission

TogglDev needs the `WRITE_SECURE_SETTINGS` permission to toggle developer options. This requires a one-time ADB command from a computer:

```
adb shell pm grant com.dpkay.apps.developer_options_toggler android.permission.WRITE_SECURE_SETTINGS
```

The app's onboarding screen walks you through this step.

### Requirements

- Android 8.0 (Oreo) or higher
- Works without Google Play Services / GMS — all core features function on any Android device

## Features

### One-tap toggles
- **Developer Options** — master on/off toggle with settings snapshot & restore
- **USB Debugging** (ADB)
- **Wireless Debugging** (ADB over WiFi) — shows connection IP:Port, tap to copy
- **Animation Scales** — window, transition, and animator duration (0x–2x)
- **Show Touches**, **Stay Awake While Plugged In**, **Force RTL Layout**, **Don't Keep Activities**, **Wait for Debugger**

### Quick Settings tiles
5 tiles you can add to your notification shade for instant access:
- Toggle Developer Options
- Toggle USB Debugging
- Toggle Wireless Debugging (shows IP:Port)
- Open Developer Settings
- Open Accessibility Settings

### Home screen widgets
5 widgets for one-tap control right from your home screen — same set as the Quick Settings tiles.

### Launcher shortcuts
Long-press the app icon for a shortcut to toggle Developer Options on/off.

### Auto-disable
Automatically turn off Developer Options when specific apps launch (e.g., banking apps). Configurable delay before re-enabling.

### Settings snapshot & restore
When you disable Developer Options, TogglDev saves all your current settings. When you re-enable, everything is restored exactly as it was.

### Multi-language
Supports 17 languages: Arabic, Chinese, Danish, Dutch, English, French, German, Greek, Indonesian, Japanese, Korean, Persian, Polish, Portuguese (BR), Russian, Thai, and Turkish.

## Links

- [Google Play Store](https://play.google.com/store/apps/details?id=com.dpkay.apps.developer_options_toggler)
- [Privacy Policy](https://dpkay.com/toggldev/privacy-policy.html)
