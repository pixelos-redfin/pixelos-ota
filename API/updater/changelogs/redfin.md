**Changes**
* Play Store keeps seeing the real Pixel 5, so it keeps offering apps built for it (e.g. Google Camera). This is now a device setting instead of removed code, and the same change was submitted to PixelOS. Play Integrity is not affected.
* Leftover build system changes from earlier test builds were removed. No visible change.

**After updating**
* Check that Google Camera opens and that Play Integrity still shows BASIC (wait about 5 minutes after the first boot).

**Installing**
* This is an incremental update from 20261028-1919.
* If installing fails right after a restart, wait a few minutes and try again. The phone finishes applying the previous update in the background first.
* Coming from a build before 20261028-1919: install the factory image with `flash-all` (erases all data). A Russian installation guide is attached to the GitHub release.
