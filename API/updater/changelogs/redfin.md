**Fixes**
* Play Store now sees the real Pixel 5, so it installs app versions built for it. This fixes Google Camera crashing at launch with "Device is not recognized or not supported".
* Silenced a harmless sensors SELinux denial in the logs

**After updating**
* If Google Camera crashes, uninstall it once and install it again from Play Store. Play Store does not replace the incompatible version that is already installed.

**Installing**
* This is an incremental update from 20261027-1820.
* Coming from a build before 20261027-1820: install the factory image with `flash-all` (erases all data).
