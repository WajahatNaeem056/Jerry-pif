# jerry-pif-inject

Derived from KOWX712/PlayIntegrityFix (branch `inject_s`, GPL-3.0), which is based on chiteroman's PlayIntegrityFix.

Changes:
- Module path changed to `/data/adb/modules/JerryManager/`.
- Removed the module.prop CRC32 tamper check (`verifyModule`, `checksum.h`, `generateModulePropChecksum`).
- WebUI sources and upstream workflows removed (JerryManager ships its own WebUI).

Build: run the "Build" workflow (Actions -> Build -> Run workflow), download the `jerry-pif-inject` artifact
(`classes.dex` + `zygisk/*.so`) and copy them into the JerryManager module (`classes.dex` at root, `.so` in `zygisk/`).
Needs JDK 21, Android SDK 37, NDK 30.0.16248370, CMake 4.1.2 (Gradle fetches them on the CI runner).
