**Fixes**
* Play Integrity props that you paste in Developer options in the PlayIntegrityFix format now work. The security patch date, first SDK level, release and incremental version are applied, and option keys like spoofBuild no longer fill the logs with errors.
* Fixed a rare crash of Google Play services' integrity check when the props were read twice in one process.

**Unchanged**
* Play Integrity with the built-in PixelOS props works as before (BASIC).

**KernelSU-Next**
* If the KernelSU-Next manager says "manager version 5 is too low", install the newer manager v3.4.2-50 (official KernelSU-Next test build): https://drive.google.com/open?id=1h6c2AN_bQN5-KHHIXV5I8mcIezCqLW0Q Root keeps working either way.

**Installing**
* This is an incremental update from 20261028-1500.
* Coming from a build before 20261028-1500: install the factory image with `flash-all` (erases all data).
