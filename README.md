# TempoTracker builds

Auto-released unsigned iOS `.ipa` builds of [TempoTracker](https://github.com/Minchaka27/tempo-time-tracker), intended for **LiveContainer** and **Sideloadly** sideloading on a free Apple ID (no paid developer account required).

The `.ipa` is **not signed** — it is re-signed on-device by LiveContainer / Sideloadly with your Apple ID.

## Install via LiveContainer

1. Get the latest download URL from the [Releases](../../releases) page.
2. Open **LiveContainer** on your iPhone.
3. Tap **Install via URL** and paste the URL ending in `.ipa`.
4. LiveContainer downloads, signs with your Apple ID, and installs.

The same URL works with **Sideloadly** (drag the `.ipa` after downloading it, or use the "Install via URL" path).

## Releases

| Version | Date | URL |
|---|---|---|
| [v1.0.0](../../releases/tag/v1.0.0) | initial | `https://github.com/Minchaka27/tempo-builds/releases/download/v1.0.0/TempoTracker-1.0.ipa` |

## How it is built

See [`scripts/release-ipa.sh`](https://github.com/Minchaka27/tempo-time-tracker/blob/main/scripts/release-ipa.sh) in the source repo. Each release is a fresh unsigned build produced by `xcodebuild` and packaged with `ditto`.
