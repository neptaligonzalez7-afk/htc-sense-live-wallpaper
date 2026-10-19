# HTC Sense Bokeh Live Wallpaper (Android)

**Live wallpaper** inspired by HTC Sense **Bokeh** (Mode10). Rewritten in Java/OpenGL for **64-bit** phones where the original 32-bit native wallpaper cannot run.

> **Not affiliated with HTC.** Same aesthetic goal; new implementation.

**Related:** [HTC Weather Flip Clock](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock) — Sense-style home-screen widget with Open-Meteo weather.

## Screenshots

| Rainbow | Ocean blue | Crimson red |
|---------|------------|-------------|
| ![Rainbow live wallpaper](./screenshots/rainbow.jpg) | ![Ocean blue live wallpaper](./screenshots/ocean-blue.jpg) | ![Crimson live wallpaper](./screenshots/crimson.jpg) |

Lock screen / home screen may show your clock and weather widgets; the wallpaper is the bokeh gradient behind them.

## Download

Get builds from **[Releases](https://github.com/neptaligonzalez7-afk/htc-sense-live-wallpaper/releases)**.

All variants share package **`com.htc.android.wallpaper`**. Only **one** APK can be installed at a time (installing another **replaces** the app).

| Variant | File | versionCode | versionName | Description |
|---------|------|-------------|-------------|-------------|
| **Rainbow** | `HTC-Sense-LiveWallpaper-android36.apk` | **74** | `1.04-rainbow` | Classic multi-color Sense look (original thumbnail style) |
| **Ocean blue** | `HTC-Sense-LiveWallpaper-ocean-blue.apk` | **70** | `1.01-ocean-blue` | Smooth blue gradient; depth-of-field bubbles |
| **Crimson red** | `HTC-Sense-LiveWallpaper-crimson.apk` | **75** | `1.03-crimson` | Red gradient with lighter highlight (top-right) |

Pick the color you want from **Releases** (each variant has its own download). **Releases → Latest** highlights **ocean blue** as the default blue build; **rainbow** and **crimson** are on their own release pages.

## Requirements

- Android **7.0+** (API 24), **targetSdk 36**
- **Live wallpaper** support (standard on Samsung One UI and most launchers)

## Install

1. Download a variant from **Releases**.
2. Allow **Install unknown apps** for your browser or Files app if prompted.
3. Install the APK.
4. **Wallpapers** → **Live wallpapers** → **HTC Sense** (or your launcher’s wallpaper picker).
5. After an upgrade, if the look does not update, pick another wallpaper briefly, then select **HTC Sense** again.
6. **Switching colors** (rainbow, blue, or red)? Uninstall the existing **HTC Sense** wallpaper app first, then install the new APK.

## Variants explained

- **Rainbow** — Classic HTC Sense multi-color gradient (like the original Bokeh thumbnail).
- **Ocean blue** — Royal/azure gradient (smooth shader background, no banding).
- **Crimson** — Same bubble field and focus behavior; red tones with a stronger light side.

Bubbles are white/translucent; color comes from the background. Some medium/large orbs use a sharper “in focus” rim for depth.

## Troubleshooting

| Symptom | What to try |
|---------|-------------|
| Black or frozen wallpaper | Re-select **HTC Sense** in the picker; reboot once. |
| Still shows old colors after install | Uninstall → reinstall → pick wallpaper again. |
| “App not installed” | Often a **version downgrade**: use the newest release for that color (e.g. crimson **v75+** after rainbow **v74**). If it still fails, uninstall **HTC Sense** wallpaper, then retry. |
| Won’t install a different color | Same package for all colors — install only if the new APK’s **versionCode** is **≥** what is on the phone, or uninstall first. |

## Signing

APKs are **debug-signed** for sideloading. They are not Play Store builds.

## License

See [LICENSE](./LICENSE). HTC Sense names and assets are trademarks of their respective owners.

## Reporting issues

Open a **GitHub Issue** with device model, **Android version**, launcher name, **APK filename**, and a short screen recording of the wallpaper (home + lock screen if relevant).

## Support (optional)

If this wallpaper is useful on your phone, you can [buy me a coffee](https://buymeacoffee.com/neta4457). Thanks for trying it.
