# Setup — htc-sense-live-wallpaper (GitHub)

APK-only public repo (same pattern as `htc-weather-flip-clock`). Source and build scripts stay in the private/local `HTC` tree; users get README + **Releases**.

## Repo

- **Name:** `htc-sense-live-wallpaper`
- **URL:** https://github.com/neptaligonzalez7-afk/htc-sense-live-wallpaper

## One release per color (current)

| Tag | Title | APK asset |
|-----|--------|-----------|
| `live-wallpaper-rainbow-v74` | Sense Bokeh — Rainbow | `HTC-Sense-LiveWallpaper-android36.apk` |
| `live-wallpaper-ocean-v70` | Sense Bokeh — Ocean Blue | `HTC-Sense-LiveWallpaper-ocean-blue.apk` |
| `live-wallpaper-crimson-v75` | Sense Bokeh — Crimson | `HTC-Sense-LiveWallpaper-crimson.apk` |

Mark **ocean blue** or the variant you want as **Latest** (`gh release edit … --latest`).

## When publishing an updated APK

**Delete the previous release for that color** so GitHub only lists one download (same filename, higher `versionCode`).

```powershell
# Example: replacing crimson v75 with v76 later
gh release delete live-wallpaper-crimson-v75 --repo neptaligonzalez7-afk/htc-sense-live-wallpaper --yes --cleanup-tag
gh release create live-wallpaper-crimson-v76 --repo neptaligonzalez7-afk/htc-sense-live-wallpaper `
  --title "Sense Bokeh — Crimson (v76)" `
  --notes-file release-notes-crimson-v76.md `
  "c:\Users\ngonz26\Documents\HTC\HTC-Sense-LiveWallpaper-crimson.apk"
```

If an old tag remains without a release (orphan tag), remove it:

```powershell
gh api -X DELETE "repos/neptaligonzalez7-afk/htc-sense-live-wallpaper/git/refs/tags/live-wallpaper-rainbow-v54"
```

Update README version table and commit on `main`.

## Build APKs locally

From `c:\Users\ngonz26\Documents\HTC`:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File build_sense_ocean.ps1
powershell -NoProfile -ExecutionPolicy Bypass -File build_sense_crimson.ps1
powershell -NoProfile -ExecutionPolicy Bypass -File build_sense_rainbow.ps1
```

Outputs in project root: `HTC-Sense-LiveWallpaper-*.apk` (do **not** commit to git — attach to Releases).

## GitHub CLI example (new color version)

```powershell
cd "c:\Users\ngonz26\Documents\HTC\github-export\htc-sense-live-wallpaper"
gh release create live-wallpaper-ocean-v71 `
  "c:\Users\ngonz26\Documents\HTC\HTC-Sense-LiveWallpaper-ocean-blue.apk" `
  --title "Sense Bokeh — Ocean Blue (v71)" `
  --notes-file release-notes-ocean-blue.md `
  --latest
```

## Do not publish

- Keystores, `.env`, ADB IPs
- Full `lwp/decoded` smali tree (optional separate source repo later)
