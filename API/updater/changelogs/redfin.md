**Fixes**
* The PixelOS boot animation now also plays with dark theme on. Before, dark theme showed the stock "android" animation.
* Wakeups from voice hotword detection are now counted in wakeup statistics, which helps track down battery drain.
* Fixed a repeating SELinux error when the system UI checks for Bluetooth Find My Device support.

**Improvements**
* KernelSU now hooks the kernel directly instead of through kprobes. This removes overhead from system calls in apps, so the system should feel a little lighter.

**Changes**
* The Updater icon is removed from the app drawer. Updates are still in Settings > System > System updates and in notifications.
* KernelSU's optional "adb root" toggle no longer works with the new hook method. Root, su, modules and the KernelSU manager work as before.

**After updating**
* Open the KernelSU manager and check that it shows "Working".

**Installing**
* This is an incremental update from 20261028-0515.
* Coming from a build before 20261028-0515: install the factory image with `flash-all` (erases all data).
