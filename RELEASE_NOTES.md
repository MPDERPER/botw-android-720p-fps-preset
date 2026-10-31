# v1.2.0 — shader and render-distance optimization update

Updated MPDERPER's Breath of the Wild Android FPS optimizer while preserving MaxLastBreath's unchanged UltraCam payload.

- Configured gameplay resolution: **1280 × 720**.
- Gameplay and menu caps: **59 FPS**.
- Retains `ShadowResolution = 206` for reduced shadow rendering cost, with a potential visual-quality tradeoff.
- Disables ambient occlusion, screen-space reflections, volumetric fog, and bloom.
- Reduces `RenderDistance` from `10000` to `5000`.
- Reduces `Fov` from `55` to `45`.
- Enables the **1280 × 720 handheld/portable override**.
- Retains `QualityImprovements = On`.
- Disables controller-triggered free-camera controls.

The shader changes, reduced render distance, and narrower field of view trade visual quality and visible scene detail for lower rendering cost. The 59 FPS value is a configuration target, not a performance guarantee. No Android device, emulator build, game session, or independent benchmark was tested for this release.

Extract the attached ZIP and install the `BOTW Android 720p FPS Optimizer` folder through your emulator's per-game mod management, preserving `exefs` and `romfs`. See the repository README for conflicts and compatibility limitations.

**Credits:** UltraCam / NX Optimizer by [MaxLastBreath](https://github.com/MaxLastBreath/nx-optimizer); Android configuration and packaging by MPDERPER. Upstream binaries are redistributed unchanged under [CC BY-NC 2.0](https://creativecommons.org/licenses/by-nc/2.0/). No game ROM, update, keys, firmware, emulator, or game assets are included.


