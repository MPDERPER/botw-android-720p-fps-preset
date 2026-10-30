# BOTW Android 720p FPS Preset

An Android-focused UltraCam configuration preset packaged by **MPDERPER** for *The Legend of Zelda: Breath of the Wild*. It targets **1280 × 720**, uses a **59 FPS gameplay and menu cap**, enables the handheld/portable resolution override, and applies settings intended to reduce rendering cost. The underlying UltraCam implementation is by **MaxLastBreath**.

This repository does not claim a measured performance result. The 59 FPS setting is a cap and target, not a promise of sustained 59 or 60 FPS. Actual performance depends on the Android device, emulator build, graphics driver, game version, scene, thermal limits, and other settings.

## Settings included

The supplied `maxlastbreath.ini` is preserved byte-for-byte.

| Setting | Value | Meaning / limitation |
| --- | --- | --- |
| Resolution | `Width = 1280`, `Height = 720` | Configured 720p rendering target; actual behavior depends on UltraCam and emulator settings. |
| Gameplay cap | `MaxFramerate = 59` | Requested maximum frame rate. |
| Menu cap | `MenuFPS = 59` | Requested menu frame-rate limit. |
| Quality options | `QualityImprovements = On` | Enables the named UltraCam quality option. |
| Render distance | `RenderDistance = 10000` | Configured render distance; no measured performance gain is claimed. |
| Field of view | `Fov = 55` | Preset camera field of view. |
| Free-camera controls | `TriggerWithController = Off` | Disables the controller trigger for UltraCam free-camera functionality. |
| Handheld / portable mode | `Width = 1280`, `Height = 720`, `OverrideHandheld_Resolution = On` | Requests the 1280 × 720 portable-mode override. |
| Benchmark selector | `Benchmark = 1` | A configuration value only; no benchmark was run for this release. |

These are configuration choices, not independently measured improvements.

## Installation on Android

The exact menu name varies by emulator build. These instructions describe the required mod layout and have not been tested in a live Android session.

1. Back up your saves and existing mod configuration, then close the game.
2. Download and extract the release ZIP. The folder `BOTW FPS PRESET ANDROID 720P` must contain `exefs` and `romfs` directly beneath it.
3. Use your emulator's per-game mod/add-on manager to install or select that folder. If the emulator uses a mod directory, place the complete folder in the game's mod/load directory without changing its internal layout.
4. Disable other mods that replace `exefs/main.npdm`, `exefs/subsdk3`, or the same UltraCam INI. Avoid stacking conflicting FPS, resolution, or dynamic-FPS mods.
5. Enable the preset and check game speed, stability, image quality, thermals, and frame pacing. Disable it and restore your backup if problems occur.

```text
BOTW FPS PRESET ANDROID 720P/
├── exefs/
│   ├── main.npdm
│   └── subsdk3
└── romfs/
    └── UltraCam/
        └── maxlastbreath.ini
```

The two binaries match MaxLastBreath's public BOTW UltraCam payload. Exact game-update and emulator compatibility has not been independently established. Consult [MaxLastBreath's upstream project](https://github.com/MaxLastBreath/nx-optimizer) for current compatibility guidance.

This release includes no emulator, GPU driver, game, update, firmware, keys, ROM, textures, models, music, screenshots, or other game media assets.

## Credits and redistribution

- **MPDERPER:** supplied the Android 720p configuration and packaging.
- **MaxLastBreath:** UltraCam and NX Optimizer, including the unchanged upstream binaries. See [CREDITS.md](CREDITS.md).

The bundled upstream material is distributed under **Creative Commons Attribution-NonCommercial 2.0 Generic (CC BY-NC 2.0)**. Preserve attribution and license notices and do not use it commercially. See [LICENSING.md](LICENSING.md), [the original license notice](LICENSE.upstream.md), and [PROVENANCE.md](PROVENANCE.md). No endorsement by MaxLastBreath, Nintendo, or any emulator project is claimed.

## Validation

Static checks verified the archive structure, exact file copies, binary matches to the pinned upstream source, and release ZIP integrity. **No game launch, Android-device test, or independent performance benchmark was performed.**