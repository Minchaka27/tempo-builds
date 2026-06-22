# TempoTracker builds

Auto-released unsigned iOS `.ipa` builds of [TempoTracker](https://github.com/Minchaka27/tempo-time-tracker), intended for **LiveContainer** and **Sideloadly** sideloading on a free Apple ID (no paid developer account required).

The `.ipa` is **not signed** — it is re-signed on-device by LiveContainer / Sideloadly with your Apple ID.

## Install / Update via LiveContainer (recommended)

LiveContainer 3.5+ supports AltStore-format **Sources** for auto-update.

1. Open **LiveContainer** on your iPhone.
2. Go to **Sources** tab -> `+`.
3. Add this URL:

   ```
   https://raw.githubusercontent.com/Minchaka27/tempo-builds/main/source.json
   ```

4. Tap **TempoTracker** -> **Install** (or **Update** if already installed).

Future releases will show up as "Update available" in LiveContainer - just tap **Update**.

**One-tap deep link** (open on the iPhone to add the source automatically):

```
livecontainer://source?url=https%3A%2F%2Fraw.githubusercontent.com%2FMinchaka27%2Ftempo-builds%2Fmain%2Fsource.json
```

## Manual install via Sideloadly

1. Download the `.ipa` from the [Releases](../../releases) page.
2. Drag it into **Sideloadly** with your Apple ID.

## Releases

| Version | Date | URL |
|---|---|---|
| [v1.0.0](../../releases/tag/v1.0.0) | 2026-06-22 | `https://github.com/Minchaka27/tempo-builds/releases/download/v1.0.0/TempoTracker-1.0.ipa` |

## How it is built

See [`scripts/release-ipa.sh`](https://github.com/Minchaka27/tempo-time-tracker/blob/main/scripts/release-ipa.sh) in the source repo. Each release is a fresh unsigned build produced by `xcodebuild` and packaged with `ditto`. The script also updates `source.json` so LiveContainer picks up the new version automatically.

