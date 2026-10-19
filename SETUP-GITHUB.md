# Setup — htc-sense-live-wallpaper (GitHub)

APK-only public repo (same pattern as `htc-weather-flip-clock`). Source and build scripts stay in the private/local `HTC` tree; users get README + **Releases**.

## Repo

- **Name:** `htc-sense-live-wallpaper`
- **URL:** https://github.com/neptaligonzalez7-afk/htc-sense-live-wallpaper

## Release tags (suggested)

| Tag | Title | APK asset |
|-----|--------|-----------|
| `live-wallpaper-ocean-v70` | Sense Bokeh — Ocean Blue | `HTC-Sense-LiveWallpaper-ocean-blue.apk` |
| `live-wallpaper-crimson-v69` | Sense Bokeh — Crimson | `HTC-Sense-LiveWallpaper-crimson.apk` |
| `live-wallpaper-rainbow-v54` | Sense Bokeh — Rainbow (archive) | `HTC-Sense-LiveWallpaper-android36.apk` |

Mark **ocean blue** as **Latest** unless you intentionally promote another variant.

## Build APKs locally

From `c:\Users\ngonz26\Documents\HTC`:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File build_sense_ocean.ps1
powershell -NoProfile -ExecutionPolicy Bypass -File build_sense_crimson.ps1
```

Outputs in project root: `HTC-Sense-LiveWallpaper-*.apk` (do **not** commit to git — attach to Releases).

## GitHub CLI example

```powershell
cd "c:\Users\ngonz26\Documents\HTC\github-export\htc-sense-live-wallpaper"
gh release create live-wallpaper-ocean-v70 `
  "c:\Users\ngonz26\Documents\HTC\HTC-Sense-LiveWallpaper-ocean-blue.apk" `
  --title "Sense Bokeh — Ocean Blue" `
  --notes-file release-notes-ocean-blue.md `
  --latest
```

## Do not publish

- Keystores, `.env`, ADB IPs
- Full `lwp/decoded` smali tree (optional separate source repo later)
