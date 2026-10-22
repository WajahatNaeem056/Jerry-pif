Jerry-PIF

Jerry-PIF is the built-in Play Integrity Fix (Zygisk module) used by "JerryManager" (https://github.com/WajahatNaeem056/JerryManager).

It handles PIF directly through JerryManager, so there's no need to install a separate PIF module.

Credit

Based on "KOWX712/PlayIntegrityFix" (https://github.com/KOWX712/PlayIntegrityFix), using the "inject_s" branch, which is itself based on "chiteroman/PlayIntegrityFix" (https://github.com/chiteroman/PlayIntegrityFix).

Licensed under GPL-3.0. See "LICENSE" (LICENSE) for details.

Build

GitHub Actions builds "classes.dex" and the Zygisk libraries on push. Download the workflow artifact and copy the files to the following locations:

- "classes.dex" → "JerryManager/dex/classes.dex"
- "zygisk/*.so" → "JerryManager/zygisk/*.so"

Notes

Jerry-PIF is built specifically for JerryManager and isn't meant to run as a standalone module.

It reads its configuration from "/data/adb/modules/JerryManager/pif.prop". The file "/data/adb/pif.prop" can be used as an override.
