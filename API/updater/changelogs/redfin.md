**Changes**
* The framework now carries only the Play Store change on top of official PixelOS. Old experimental Play Integrity code was removed from the source history. No visible change.
* Certified props are now applied the same way as in official PixelOS.
* Factory image: the Windows installer (`flash-all.bat`) now stops before flashing if the fastboot in PATH is too old, and shows which fastboot it uses. An old fastboot made it fail with "unknown option -- skip-reboot".

**After updating**
* Check Play Integrity (wait about 10 minutes after the first boot) and that Google Camera opens.

**Installing**
* This is an incremental update from 20261029-1131.
* If installing fails right after a restart, wait a few minutes and try again. The phone finishes applying the previous update in the background first.
* Coming from a build before 20261029-1131: install the factory image with `flash-all` (erases all data). Use Android platform-tools 35 or newer. A Russian installation guide is attached to the GitHub release.
