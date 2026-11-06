# BOTW Android UltraCam 900p Docked — Quality Preset + Eden Stable Settings

This release adds my 1600 × 900 Docked quality preset and supplied Eden Stable settings for BOTW on Android.

> **IMPORTANT: THIS PRESET TARGETS BOTW UPDATE 1.6.0 ONLY.**

> **IMPORTANT: THIS IS THE 900P DOCKED PRESET. ENABLE DOCKED MODE IN EDEN STABLE BEFORE PLAYING.**

## Included files

- `BOTW Ultracam 900p FPS Optimizer.zip` — combined ExeFS/RomFS BOTW UltraCam add-on.
- `EDEN STABLE SETTINGS.ini` — Eden Stable per-game settings to import.

## UltraCam configuration

- Resolution: **1600 × 900**
- FPS and menu caps: `60`
- Shadow configuration value: `512`
- Render distance: `5000`
- FOV: `45`
- Handheld override: disabled, with 1280 × 720 handheld values preserved
- Ambient occlusion, screen-space reflections, volumetric fog, and bloom: disabled

The package uses BOTW's legacy combined layout: install the complete mod folder containing both `exefs` and `romfs` through BOTW's Eden Add-ons manager. Do not copy it into TOTK's `sdmc/UltraCam/TOTK/Config` path.

The older BOTW UltraCam executable may not implement every feature from TOTK UltraCam 3.0.0. The INI contains `ShadowResolution = 512`, but active support has not been independently verified, so this release does not promise a shadow-quality change.

No new BOTW benchmark was supplied. The 60 FPS values are configuration targets, not a guarantee of sustained performance.

## Eden Stable preset

At my direction, the same supplied `EDEN STABLE SETTINGS.ini` is included in both game releases under its original filename. The BOTW asset is byte-for-byte identical to the supplied file.

Back up the current per-game settings, import the BOTW INI through Eden's **Import Config** action, and review the values. **The supplied INI leaves Docked Mode off (`use_docked_mode = 0`), so enable Docked Mode manually for this 900p preset.** Select a compatible GPU driver, restart Eden, and verify the game.

The exported INI includes a device-specific Balemuni Apex GPU-driver path. Importing it does not install that driver; users must select a compatible installed driver for their own device.

## Installation guide

Read the complete beginner workflow in the repository's [Installation Guide — Read This First](https://github.com/MPDERPER/botw-android-720p-fps-preset#installation-guide--read-this-first).

## Credits and licensing

UltraCam and NX Optimizer were created by [MaxLastBreath](https://github.com/MaxLastBreath/nx-optimizer). I performed the Android configuration, adaptation, packaging, optimization, and testing with technical assistance from ChatGPT. The executable payload is unchanged and is redistributed under the upstream CC BY-NC 2.0 notice.

No ROM, game update, firmware, keys, emulator binary, GPU-driver binary, or Nintendo game assets are included.

## SHA-256

```text
ab9fcccc986a52b0a791324fff84939511fb9aec52e524ea08826d913b3bc665  EDEN STABLE SETTINGS.ini
a51173edf81232eca84b2bec9d9b397e01d28a2b0f184aed7341ee4ea40bd453  BOTW Ultracam 900p FPS Optimizer.zip
```
