# OKTV Player — downloads

This repository holds **installers only**. The source code stays in a private
repository.

## Latest version

| Platform | Download |
|---|---|
| macOS (Apple Silicon) | [OKTV-Player-1.3.8-arm64.dmg](https://github.com/okassama/oktv-releases/releases/download/latest/OKTV-Player-1.3.8-arm64.dmg) |
| Windows (64-bit) | [OKTV-Player-Setup-1.3.8.exe](https://github.com/okassama/oktv-releases/releases/download/latest/OKTV-Player-Setup-1.3.8.exe) |
| Android TV / phone | [OKTV-Stream-AndroidTV-2.8.29.apk](https://github.com/okassama/oktv-releases/releases/download/latest/OKTV-Stream-AndroidTV-2.8.29.apk) |

## How updates work

The apps read [`latest.json`](latest.json) from this repository:

- **Desktop** — checks shortly after launch and from Settings → Updates, then
  downloads the right installer for the platform and opens it.
- **Android** — checks Settings → About → Check for updates and downloads the
  APK inside the app.

`latest.json` is the single switch: publishing a release and pointing the
manifest at it is what makes every installed app see the update.

## Notes

- The builds are unsigned, so macOS shows the usual first-launch prompt and
  Windows SmartScreen may warn. That does not mean the files are unsafe, but
  it is the reason in-place silent updates are only fully automatic on Windows.
- Each release includes SHA-256 checksums in its description.
