# Jerry-pif

[![Build](https://github.com/WajahatNaeem056/Jerry-pif/actions/workflows/build.yml/badge.svg)](https://github.com/WajahatNaeem056/Jerry-pif/actions)
[![License: GPL-3.0](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)

Built-in **Play Integrity Fix** (Zygisk module) powering [JerryManager](https://github.com/WajahatNaeem056/JerryManager) — no separate standalone PIF module needed.

Injects into Zygote and spoofs device build properties, key attestation, and vending/GMS signals so apps see a clean, unrooted device.

## What it spoofs

| Flag | Effect |
|---|---|
| `spoofBuild` | Device build fingerprint / model |
| `spoofProps` | System properties read by integrity checks |
| `spoofVendingBuild` / `spoofVendingSdk` | Play Store / vending-specific build & SDK level |
| `spoofProvider` | Content provider identity |
| `spoofSignature` | App signature reporting |

Config is read from `/data/adb/modules/JerryManager/pif.prop`, or `/data/adb/pif.prop` as a user override.

## Build

Pushing to `main` triggers [GitHub Actions](.github/workflows/build.yml), which builds the Zygisk module and uploads the module as a downloadable artifact.

## Credits

Jerry-pif is implemented from the `inject` branch of Play Integrity Fix. Sincere thanks to:

- **chiteroman**: author of the original **Play Integrity Fix**.
- **[KOWX712](https://github.com/KOWX712/PlayIntegrityFix)**: **Play Integrity Fix** `inject` branch, which Jerry-pif is implemented from

## Maintainer

Maintained by [WajahatNaeem056](https://github.com/WajahatNaeem056) as Developer of [JerryManager](https://github.com/WajahatNaeem056/JerryManager), 

## License

Released under the [GPL-3.0 license](LICENSE).
