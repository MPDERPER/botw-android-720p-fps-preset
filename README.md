# BOTW Android UltraCam FPS Optimizer

Android-focused UltraCam presets I configured and packaged for *The Legend of Zelda: Breath of the Wild* in Eden. The existing 720p preset remains available for performance-focused use, and the prepared 900p Docked preset is a higher-quality alternative. The underlying UltraCam and NX Optimizer software is by [MaxLastBreath](https://github.com/MaxLastBreath/nx-optimizer).

**[Download the 720p release](https://github.com/MPDERPER/botw-android-720p-fps-preset/releases/tag/v1.2.0)** · **[Installation Guide — Read This First](#installation-guide--read-this-first)**

> **IMPORTANT: THE BOTW ULTRACAM PORT TARGETS GAME UPDATE 1.6.0 ONLY.**

> **IMPORTANT: THE 900P QUALITY PRESET REQUIRES DOCKED MODE IN EDEN STABLE.**

## 720p versus 900p

| Preset | Intended use | Target | Mode | FPS configuration | Shadow value |
| --- | --- | --- | --- | --- | ---: |
| **900p Docked v1.3.0** | Higher image quality | 1600 × 900 | **Docked** | Gameplay/menu cap `60` | `512` in the INI |
| **720p v1.2.0** | Lower rendering cost | 1280 × 720 | Handheld override enabled | Gameplay/menu cap `59` | `206` in the INI |

The new 900p INI also contains a render distance of 5000, FOV 45, `QualityImprovements = On`, and disabled ambient occlusion, screen-space reflections, volumetric fog, and bloom. Its handheld section remains 1280 × 720 with `OverrideHandheld_Resolution = False`.

The older BOTW UltraCam executable may not implement every option available in TOTK UltraCam 3.0.0. The 900p configuration contains `ShadowResolution = 512`, but I have not independently verified that this BOTW executable actively applies that parameter. The value is documented as a configuration value, not a guaranteed shadow-quality change.

The FPS values are caps and targets. I have not supplied a new BOTW benchmark for this release, so this repository does not promise 60 FPS or a specific performance gain.

## Downloads

### 900p Docked — v1.3.0

Publication is waiting for a separately verified BOTW Eden Stable per-game INI. The completed UltraCam ZIP will be released as `botw-ultracam-900p-docked-v1.3.0.zip`; it will not be published with a renamed TOTK preset.

### 720p — v1.2.0

- [`botw-android-720p-fps-optimizer-v1.2.0.zip`](https://github.com/MPDERPER/botw-android-720p-fps-preset/releases/download/v1.2.0/botw-android-720p-fps-optimizer-v1.2.0.zip)

The [v1.2.0 release page](https://github.com/MPDERPER/botw-android-720p-fps-preset/releases/tag/v1.2.0) remains available and is not replaced by the 900p package.

<a id="installation-guide--read-this-first"></a>

# Installation Guide — Read This First

BOTW uses a legacy combined add-on layout. Two file types must remain separate:

1. **BOTW UltraCam mod ZIP** — contains both `exefs` and `romfs`; install the complete mod folder through BOTW's Eden **Add-ons** system.
2. **Eden Stable per-game INI** — import through Eden's per-game **Import Config** action.

BOTW does not use the TOTK UltraCam 3.0.0 path `sdmc/UltraCam/TOTK/Config`. Do not copy this BOTW package into that directory.

## 1. Back up and check compatibility

1. Confirm that BOTW is using update **1.6.0**.
2. Back up your saves, current per-game settings, and existing BOTW mods.
3. Disable other UltraCam, FPS, resolution, `main.npdm`, `subsdk3`, or `romfs/UltraCam/maxlastbreath.ini` modifications.
4. For the 900p preset, plan to use **Docked Mode**.

Compatibility with other BOTW updates has not been verified and is not advertised.

## 2. Install the complete BOTW add-on

1. Download the BOTW preset ZIP for the resolution you want.
2. Extract it if your Eden build requires an unpacked add-on folder.
3. Open Eden Stable.
4. Select *The Legend of Zelda: Breath of the Wild*.
5. Open the game's properties and choose **Add-ons**.
6. Install or import the complete mod folder containing both `exefs` and `romfs`.
7. Confirm that the mod appears in the Add-ons list and enable it.
8. Disable conflicting UltraCam or FPS modifications.
9. Enable Docked Mode for the 900p preset.
10. Fully restart the game.

The prepared 900p archive has this effective structure:

```text
BOTW Android 900p Docked Optimizer/
├── exefs/
│   ├── main.npdm
│   └── subsdk3
└── romfs/
    └── UltraCam/
        └── maxlastbreath.ini
```

The `romfs` configuration is part of the same BOTW add-on. Install the entire folder through Add-ons. Do not separate the BOTW INI into TOTK's virtual-SD configuration location.

## 3. Enable Docked Mode for 900p

1. Open BOTW's per-game settings in Eden Stable.
2. Find the setting that controls Handheld/Docked mode. The exact wording can vary by Eden build.
3. Select **Docked Mode**.
4. Save the setting and restart the game or emulator if required.
5. Verify the intended profile and image resolution in your Eden build.

The 900p INI preserves `OverrideHandheld_Resolution = False`. Without Docked Mode, do not assume the advertised 1600 × 900 profile is active.

## 4. Import the BOTW Eden Stable preset

This step requires a separately exported BOTW per-game configuration. It is not `romfs/UltraCam/maxlastbreath.ini` and it must not be copied into the mod folder.

1. Back up your current BOTW per-game settings.
2. Download the BOTW Eden Stable INI from the matching release.
3. Open Eden Stable and locate BOTW.
4. Open the game's settings or properties.
5. Use Eden's supported **Import Config** action.
6. Select the BOTW INI and confirm the import.
7. Review the imported settings.
8. Verify that Docked Mode is enabled for 900p.
9. Install and select a compatible GPU driver.
10. Restart Eden and test the game.

The exact import control can vary by Eden build. Importing a preset can overwrite per-game preferences. If the exported configuration contains a path from another Android device, install and select your own compatible GPU driver manually.

## 5. GPU driver information

Custom GPU drivers are device-specific and are not included in this repository.

1. Download a driver package compatible with your GPU and Eden build from its original publisher.
2. Open Eden's **GPU Driver Manager**.
3. Install the driver ZIP.
4. Select it for BOTW.
5. Restart Eden if required.
6. Test rendering, stability, thermals, and frame pacing. Return to a known-working driver if behavior worsens.

Do not assume that a GPU-driver path from another user's exported INI exists on your device.

## 6. Verify the installation

1. Fully restart Eden Stable.
2. Launch BOTW and confirm that the game loads at normal speed.
3. Confirm that exactly one UltraCam/FPS add-on is enabled.
4. Confirm Docked Mode for the 900p preset.
5. Check image resolution, frame pacing, and input response.
6. Look for missing textures, flicker, broken shadows, or other artifacts.
7. Test an outdoor area and an indoor or shrine area.
8. If behavior is wrong, restore the backed-up settings and test without the optimizer.

## 7. Troubleshooting

- **UltraCam does not load:** verify that `exefs` and `romfs` are directly under the enabled mod folder and that the package targets BOTW update 1.6.0.
- **Settings do not change:** confirm that `romfs/UltraCam/maxlastbreath.ini` exists inside the same enabled BOTW add-on and disable duplicates.
- **The game runs in slow motion:** check Eden's emulation speed and conflicting FPS or Dynamic FPS modifications.
- **The image does not appear to be 900p:** enable Docked Mode, restart, and confirm that the 900p add-on rather than the 720p add-on is enabled.
- **Imported INI cannot find a GPU driver:** install a compatible driver and select it manually.
- **The game crashes or graphics break:** disable conflicts, return to a known-working driver, and restore your previous per-game settings.
- **Performance is below the configured cap:** the cap is not a guarantee. Reduce load, check thermals and driver behavior, or return to the 720p preset.

## Performance and visual-quality notes

The 900p preset increases the configured pixel count from 1280 × 720 to 1600 × 900 and changes the INI's shadow value from 206 to 512. This may improve image quality if the executable applies those settings, while also increasing GPU or memory load. I have not provided new BOTW benchmark figures, independently verified the shadow parameter's active support, or guaranteed sustained 60 FPS.

The 720p preset disables four shader effects, uses a render distance of 5000, and narrows FOV to 45 to reduce rendering work. Those choices trade visual quality and scene detail for lower load.

## Credits and licensing

- **MaxLastBreath:** original NX Optimizer and UltraCam development.
- **MPDERPER:** Android configuration, adaptation, packaging, optimization, and testing.
- **ChatGPT:** technical and documentation assistance.

The UltraCam binaries match MaxLastBreath's public upstream payload and are redistributed under the upstream **CC BY-NC 2.0** notice. See [credits](CREDITS.md), [licensing](LICENSING.md), [upstream notice](LICENSE.upstream.md), and [provenance](PROVENANCE.md). This unofficial project does not imply endorsement by Nintendo, Eden, or MaxLastBreath.

No ROM, game update, firmware, keys, emulator binary, GPU-driver binary, textures, models, music, screenshots, or other game assets are included.
