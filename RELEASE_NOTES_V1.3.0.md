# BOTW Android UltraCam 900p Docked — Quality Preset + Eden Stable Settings

This release is prepared but must not be published until a separate, verified BOTW Eden Stable per-game INI is supplied.

> **IMPORTANT: THIS PRESET TARGETS BOTW UPDATE 1.6.0 ONLY.**

> **IMPORTANT: THIS IS THE 900P DOCKED PRESET. ENABLE DOCKED MODE IN EDEN STABLE BEFORE PLAYING.**

## Prepared UltraCam package

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

## Required Stable preset

The intended final release must also include a separately exported and verified BOTW Eden Stable per-game configuration for title ID `01007EF00011E000`. A TOTK preset will not be renamed or reused for BOTW.

After that file is supplied, users will back up their current per-game settings, import the BOTW INI through Eden's **Import Config** action, confirm Docked Mode, select a compatible GPU driver, restart Eden, and verify the game.

## Installation guide

Read the complete beginner workflow in the repository's [Installation Guide — Read This First](https://github.com/MPDERPER/botw-android-720p-fps-preset#installation-guide--read-this-first).

## Credits and licensing

UltraCam and NX Optimizer were created by [MaxLastBreath](https://github.com/MaxLastBreath/nx-optimizer). I performed the Android configuration, adaptation, packaging, optimization, and testing with technical assistance from ChatGPT. The executable payload is unchanged and is redistributed under the upstream CC BY-NC 2.0 notice.

No ROM, game update, firmware, keys, emulator binary, GPU-driver binary, or Nintendo game assets are included.
