# Provenance and inspection

Upstream repository: https://github.com/MaxLastBreath/nx-optimizer

Pinned revision: `bd98bb3c9ee7eb16c2dd3c51a8c6ecf168330cf3`

Both supplied binary files are byte-for-byte identical to the following upstream BOTW UltraCam files at the pinned revision:

| File | Upstream Git blob SHA-1 | SHA-256 |
| --- | --- | --- |
| `main.npdm` | `a09fe367863f30d74d9f62eabc3ee4323292933c` | `7cedbb57ba93e3ab6e660490a0a7b932716854004786a2ac42d39dbf8b85e678` |
| `subsdk3` | `41b34b5ce7da414ece922d89fb7c6bf364d6c7a1` | `1216d58cb3eb8028a905a3c88b104a1338b48cff2b1dfeac571bff7b9826dac6` |

Source directory: https://github.com/MaxLastBreath/nx-optimizer/tree/bd98bb3c9ee7eb16c2dd3c51a8c6ecf168330cf3/src/PatchInfo/Breath%20Of%20The%20Wild/UltraCam/exefs

License notice: https://github.com/MaxLastBreath/nx-optimizer/blob/bd98bb3c9ee7eb16c2dd3c51a8c6ecf168330cf3/LICENSE.md

The v1.2.0 source RAR contains exactly three files: the two binaries above and `romfs/UltraCam/maxlastbreath.ini`. The v1.2.0 INI SHA-256 is `6ced7235b6a75fc0acd2ad19a4d76a51d45428431741b452e3eb6c0940887023`.

The pinned upstream tree contains `LICENSE.md`, declaring CC BY-NC 2.0. Its notice is included verbatim as `LICENSE.upstream.md`. The binary files were inspected and compared, not executed. No game assets or third-party emulator binaries were found in the supplied archive.

Validation is static only. No Android device, emulator installation, game session, or performance benchmark was run.

## Prepared v1.3.0 900p Docked package

The supplied 900p RAR contains the same two upstream executable files documented above and a new user configuration. The prepared ZIP adds only the upstream license notice.

| File | SHA-256 |
| --- | --- |
| `exefs/main.npdm` | `7cedbb57ba93e3ab6e660490a0a7b932716854004786a2ac42d39dbf8b85e678` |
| `exefs/subsdk3` | `1216d58cb3eb8028a905a3c88b104a1338b48cff2b1dfeac571bff7b9826dac6` |
| `romfs/UltraCam/maxlastbreath.ini` — 900p | `7ee836ca9f63d538ea4afe0ba33859fb55005281334235d01398371f094d66d3` |
| `botw-ultracam-900p-docked-v1.3.0.zip` | `5d5b3002c87f7fad9e5f60909b4040e112685f8a8818cd45ae37242da9be3744` |

At MPDERPER's explicit direction, the same user-supplied `EDEN STABLE SETTINGS.ini` is published under separate TOTK and BOTW filenames. The BOTW copy is byte-for-byte identical to the supplied file and has SHA-256 `ab9fcccc986a52b0a791324fff84939511fb9aec52e524ea08826d913b3bc665`. It intentionally retains `use_docked_mode\default = true`, `use_docked_mode = 0`, and `scaling_filter = 0`; 900p users must manually enable Docked Mode after import. The Eden export does not contain a Nintendo title ID, so this game-specific use follows the user's explicit instruction rather than an embedded identifier.


