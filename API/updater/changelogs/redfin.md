**Fixes**
* Play Integrity props are updated again. The system couldn't read the PixelOS version, so every download of the official PixelOS props failed and phones kept using old props. They now download within 5 minutes after boot and refresh every 5 minutes.
* When the developer option that turns off certified props is on, the phone also stops downloading them.

**After updating**
* Wait about 5 minutes after the first boot, then check Play Integrity again.

**Installing**
* This is an incremental update from 20261028-1746.
* If installing fails right after a restart, wait a few minutes and try again. The phone finishes applying the previous update in the background first.
* Coming from a build before 20261028-1746: install the factory image with `flash-all` (erases all data).
