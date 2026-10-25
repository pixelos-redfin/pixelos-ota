# PixelOS 17.0 for Pixel 5 (redfin)

### 2026-10-25 Hotfix (Native Play Integrity Fix)
- Built-in Certified Properties (`config_certifiedBuildProperties`) passing Device & Basic integrity out-of-the-box with zero root modules required
- Revoked beta fingerprint guard in `PropImitationHooks` to automatically prevent blacklisted prints from breaking attestation
- Robust key attestation interception for Google Play Services to guarantee software fallback
- Incremental delta update package (~43 MB)

### 2026-10-25 Update (KernelSU + SUSFS Delta)
- Integrated KernelSU-Next with SUSFS (`CONFIG_KSU=y`, `CONFIG_KSU_SUSFS=y`)
- Fixed Play Integrity Certified Properties overlay error ("Downloaded package is invalid")
- Play Integrity vbmeta digest: `85cc15ae0b4c49a7027cf5306d48d34749dc6ee4d026102c358d2e01805d9fd6`

### 2026-10-24 Update
- Seamless Incremental and Full OTA Updates support via PixelOS Updater
- Direct GitHub Releases and CDN multi-hop redirect handling
- Modernised kernel parameters: 4GB ZRAM with LZ4 compression
- Smooth frame pacing with schedutil down rate limit tuning
- Fixed seccomp policy crash dump issues on codec2
- Restored Google Battery service and VINTF integration
