# Device status and development plans

Updated 29 September 2026. ReMeizu develops Android 9, 11 and 13 ports for older
Meizu phones and investigates upstream Linux/postmarketOS support. The roadmap
covers 17 models across six chipset families; support varies by device.

## Current work

| Device / track | Working result | Next work |
|---|---|---|
| MX6 / M95, Android 13 | Native LOS20 boots; LTE data and IMS registration observed on build 23 | Test incoming-call and camera changes; camera, suspend and battery validation |
| M5c, Android 13 / Linux 4.9 | Boot, display, touch and Wi-Fi scanning observed on hardware | Complete connectivity, audio, camera and power testing |
| M5s, Linux 4.9 | Kernel links and produces Image.gz; board/display work compiles | Validate the DTB and boot image, then test on hardware |
| U10, Linux 3.18 | Touch and power objects compile | Apply the published patch series and complete the board port |
| U20, Linux 3.18 | Charger transport compiles against the kernel API; board resource and status-read work in development | Complete charger ownership and battery policy, then full board build |
| M3s / U10 / U20, Android 9 | Product and build-graph checks pass | Kernel/vendor integration and complete ROM builds |
| M5s / M2 Note, Android 9 | Full-ROM build work in progress | Resolve remaining build failures and produce testable images |
| Other Android 11 / 13 tracks | Device configuration and compatibility sources published | Complete builds and device testing |

A compiled object or kernel is not a tested phone image. The source repositories
contain development work and may require additional kernel, vendor and common-tree
inputs. Downloadable releases are listed separately in
[remeizu-releases](https://github.com/nomorecoolnicknames/remeizu-releases/releases).

## Priorities

1. Establish usable LOS16 / Android 9 baselines, then improve Android 11 and 13.
2. Share common support across MT6735/6737, MT6753 and MT6750/6755 while preserving
   board-specific PMIC, display, sensor and memory differences. MT6752, MT6797 and
   Qualcomm MSM8953 remain separate tracks.
3. Replace practical host-driver and HAL dependencies with open implementations;
   see the [component roadmap](OPEN_COMPONENTS_ROADMAP.md).
4. Bring up upstream Linux in stages: boot, storage, USB, power, then display,
   input and connectivity. Submit tested driver and board changes upstream and
   use those foundations for postmarketOS ports.
5. Expand automated builds and device regression tests. Flashing, recovery and
   hardware acceptance still need device-specific checks.

[Source repositories](SOURCE_INDEX.md) · [Build infrastructure](BUILD_INFRASTRUCTURE.md)
