# PixelOS 17.0 for Pixel 5 (redfin)

### 2026-10-25 Update (Incremental Delta OTA)
- Integrated KernelSU-Next with SUSFS (`CONFIG_KSU=y`, `CONFIG_KSU_SUSFS=y`)
- Fixed Play Integrity Certified Properties overlay error ("Downloaded package is invalid")
- Play Integrity vbmeta digest: `85cc15ae0b4c49a7027cf5306d48d34749dc6ee4d026102c358d2e01805d9fd6`
- Incremental delta update from `PixelOS_redfin-17.0-20261024-2237` (~80 MB)

### 2026-10-24 Update
- Seamless Incremental and Full OTA Updates support via PixelOS Updater
- Direct GitHub Releases and CDN multi-hop redirect handling
- Modernised kernel parameters: 4GB ZRAM with LZ4 compression
- Smooth frame pacing with schedutil down rate limit tuning
- Fixed seccomp policy crash dump issues on codec2
- Restored Google Battery service and VINTF integration
