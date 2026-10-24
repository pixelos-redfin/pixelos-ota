# pixelos-ota

Official OTA feed and changelogs for **PixelOS on Google Pixel 5 (redfin)**.

Consumed by the PixelOS Updater app (`net.pixelos.ota`). The app constructs its URLs from:

```text
https://raw.githubusercontent.com/pixelos-redfin/pixelos-ota/{branch}/API/updater/{device}.json
https://raw.githubusercontent.com/pixelos-redfin/pixelos-ota/{branch}/API/updater/changelogs/{device}.md
```

- `{branch}` resolves to `net.pixelos.version` (`seventeen`).
- `{device}` resolves to `ro.custom.device` (`redfin`).

## Layout

```text
API/
└── updater/
    ├── redfin.json                  # Feed entry (Full & Incremental)
    └── changelogs/
        └── redfin.md                # Markdown changelog displayed in Updater
README.md
```

## Feed Schema (with Incremental OTA support)

```json
[
  {
    "datetime": 1792831815,
    "version": "17.0",
    "type": "ci",
    "files": [
      {
        "filename": "PixelOS_redfin-17.0-20261024-0852.zip",
        "os_patch_level": "2026-10-01",
        "os_sdk_level": 37,
        "sha256": "79868165894e2c50ee53e799acac4fec63d272f4a532ebb209441ff4f3d37187",
        "size": 2460833368,
        "url": "https://github.com/pixelos-redfin/pixelos-ota/releases/download/20261024-0852/PixelOS_redfin-17.0-20261024-0852.zip",
        "ota_property_files": "payload_metadata.bin:4038:159635,payload.bin:4038:2460827778,payload_properties.txt:2460831874:156,apex_info.pb:1938:1498,care_map.pb:3483:508,metadata:69:672,metadata.pb:809:1081"
      }
    ],
    "incremental": [
      {
        "filename": "PixelOS_redfin-incremental-20261021-to-20261024.zip",
        "os_patch_level": "2026-10-01",
        "os_sdk_level": 37,
        "sha256": "...",
        "size": 154823901,
        "url": "https://github.com/pixelos-redfin/pixelos-ota/releases/download/20261024-0852/PixelOS_redfin-incremental-20261021-to-20261024.zip",
        "ota_property_files": "payload_metadata.bin:4038:159635,payload.bin:4038:154820000,payload_properties.txt:154821500:156,..."
      }
    ]
  }
]
```

### How Incremental Updates Work
1. When a user checks for updates in Updater, Updater fetches `redfin.json`.
2. On A/B devices (like Pixel 5), Updater inspects the `incremental` entry.
3. Updater performs a lightweight HTTP range request (`bytes=offset-(offset+size-1)`) for `payload_metadata.bin` and submits it to `update_engine.verifyPayloadMetadata()`.
4. If the device's currently installed build matches the source build of the delta, `update_engine` verifies and accepts it.
5. The incremental delta (~50-200 MB) is downloaded and streamed directly to the inactive slot.
6. If the incremental update fails at any point or does not apply to the device's current build, Updater cleanly falls back to downloading the full update package.
