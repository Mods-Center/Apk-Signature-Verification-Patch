## v4 (9)

Disable APK signature verification — v4 (versionCode 8). Hotfix for #4.

- Fixed install failing with `OutOfMemoryError` while decompiling services.jar on some Android 16 ROMs: APKEditor now loads one dex at a time, and retries with a bigger heap if it still runs out of memory.
- Fixed the `XdConfig` helper class being silently skipped on Magisk/KernelSU (busybox `sort` has no `-V`). Without it framework.jar could fail at boot; the installer now aborts instead of ever installing such a jar.

Previous v4 notes:


- Complete APKEditor 1.4.9 engine (fixes "Decompile failed / inStream parameter is null" at install).
- Install-time integrity gate: aborts safely if the rebuilt jar's non-code resources change, instead of installing a jar that crashes at boot (e.g. `Failed to parse debian.mime.types`).
- Keep a downgraded system-app update after reboot.

## v4 (8)

Disable APK signature verification — v4 (versionCode 6).

- Complete APKEditor 1.4.9 engine (fixes "Decompile failed / inStream parameter is null" at install).
- Install-time integrity gate: aborts safely if the rebuilt jar's non-code resources change, instead of installing a jar that crashes at boot (e.g. `Failed to parse debian.mime.types`).
- Keep a downgraded system-app update after reboot.

## v4 (7)

### Changelogs 
**Nov 16, 2026**
- Added a safety check: this module and the Apk Protection Patch module cannot be installed at the same time (they modify the same system files). Flashing the second one now shows an error.

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

