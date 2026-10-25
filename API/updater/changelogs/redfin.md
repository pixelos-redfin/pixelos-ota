This update includes security and device certification improvements for your Pixel 5.

**Device Integrity & Attestation**
* Fixed an issue where Google Play Integrity only reported `MEETS_BASIC_INTEGRITY` after installing a system update
* Synchronized security patch levels across Google Play Store and hardware Keystore certificate chains for `MEETS_DEVICE_INTEGRITY` and `MEETS_STRONG_INTEGRITY`
* Added automatic refresh of cached Google Play Store attestation keys on startup
* Fixed hardware TEE Root of Trust (`verifiedBootKey`) verification when generating certificate chains

**System & Boot Properties**
* Standardized Verified Boot lock state and SELinux enforcing status across vendor and system boot properties
