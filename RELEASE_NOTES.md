# v1.1.0 — shadow optimization update

Updated MPDERPER's Breath of the Wild Android FPS optimizer while preserving MaxLastBreath's unchanged UltraCam payload.

- Configured gameplay resolution: **1280 × 720**.
- Gameplay and menu caps: **59 FPS**.
- Adds `ShadowResolution = 206` for reduced shadow rendering cost, with a potential visual-quality tradeoff.
- Enables the **1280 × 720 handheld/portable override**.
- Uses `QualityImprovements = On`, `RenderDistance = 10000`, and `Fov = 55`.
- Disables controller-triggered free-camera controls.

The 59 FPS value is a configuration target, not a performance guarantee. No Android device, emulator build, game session, or independent benchmark was tested for this release.

Extract the attached ZIP and install the `BOTW Android 720p FPS Optimizer` folder through your emulator's per-game mod management, preserving `exefs` and `romfs`. See the repository README for conflicts and compatibility limitations.

**Credits:** UltraCam / NX Optimizer by [MaxLastBreath](https://github.com/MaxLastBreath/nx-optimizer); Android configuration and packaging by MPDERPER. Upstream binaries are redistributed unchanged under [CC BY-NC 2.0](https://creativecommons.org/licenses/by-nc/2.0/). No game ROM, update, keys, firmware, emulator, or game assets are included.

