This update moves your Pixel 5 to PixelOS release keys and adds support for a locked bootloader.

**Security**
* System, apps and system modules are now signed with private PixelOS release keys instead of public test keys
* Verified boot is enabled; the bootloader can be relocked with the PixelOS boot key (a yellow notice is shown at startup)
* Removed experimental Play Integrity attestation workarounds; certified properties now come from upstream PixelOS

**Installing**
* Coming from an earlier build: install the factory image with `flash-all` (erases all data). Earlier builds use different keys and cannot update over the air.
* The phone must run the latest stock Android 14 firmware (UP1A.231105.001.B2) before installing.
