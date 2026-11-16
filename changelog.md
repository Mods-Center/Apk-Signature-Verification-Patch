## v4 (6)

### Changelogs 
**Nov 16, 2026**
- Fixed "Decompile failed / inStream parameter is null" on install - the bundled APKEditor 1.4.9 engine was missing its resource files; it is now complete.
- Fixed random system crashes on some devices (e.g. MediaStore/WebView `Failed to parse debian.mime.types`). The rebuilt system jar is now verified before install: if the on-device rebuild alters any non-code resource, the module aborts safely instead of installing a jar that crashes at boot.
- Updated the on-device APKEditor engine to 1.4.9 (more reliable jar rebuilds).
- Keep a downgraded update of a system app after a reboot (previously it was reverted to the stock version and uninstalled on boot).

**Nov 6, 2025**
- Improved codes for ColorOS roms
- Added support for Android 16
- Added support for modifying **framework.jar** , **services.jar** and **miui-services.jar**(optional) directly.
- To Modify Non-System Jars, Place your JAR file inside **`/sdcard/mods_center/`** and flash the module.

**16 Feb, 2026**
- Making the module completely offline, everything added in the module.

