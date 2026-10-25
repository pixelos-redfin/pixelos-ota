# PixelOS 17.0 for Pixel 5 (redfin)

### 2026-10-25 Update (Delta OTA)
- Integrated KernelSU-Next (origin/legacy branch for Linux 4.19)
- Fixed Play Integrity Certified Properties overlay error ("Downloaded package is invalid")
- Play Integrity vbmeta digest: `85cc15ae0b4c49a7027cf5306d48d34749dc6ee4d026102c358d2e01805d9fd6`
- Applied incremental delta update (13 MB)

### 2026-10-24 Update
- Seamless Incremental and Full OTA Updates support via PixelOS Updater
- Direct GitHub Releases and CDN multi-hop redirect handling
- Modernised kernel parameters: 4GB ZRAM with LZ4 compression
- Smooth frame pacing with schedutil down rate limit tuning
- Fixed seccomp policy crash dump issues on codec2
- Restored Google Battery service and VINTF integration
