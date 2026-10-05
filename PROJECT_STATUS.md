# Device status and development plans

Updated 6 October 2026. ReMeizu develops Android 9, 11 and 13 ports for older
Meizu phones and investigates upstream Linux/postmarketOS support. The roadmap
covers 16 catalogue entries across five chipset groups; support varies by device.

## Current work

| Device / track | Working result | Next work |
|---|---|---|
| MX6 / M95, Android 13 | Native LOS20 boots; LTE data and IMS registration observed on build 23 | Test incoming-call and camera changes; camera, suspend and battery validation |
| M5c, Android 13 / Linux 4.9 | Boot, display, touch and ADB; Wi-Fi scan, Bluetooth enabled and LTE registration/data context observed; SELinux permissive | No usable camera image; microphone capture fails; test Wi-Fi association, Bluetooth pairing and cellular traffic |
| M3 Note L681, Android 9 / Linux 4.4 | Boots to the launcher with verified boot readback; nine sensors reported and Wi-Fi scanning observed | Cameras unavailable; test Wi-Fi connection, audio and power behavior |
| M5s, Linux 4.9 | Kernel links and produces Image.gz; board/display work compiles | Validate the DTB and boot image, then test on hardware |
| M3s, Android 9 | Product and build-graph checks pass | Kernel/vendor integration and complete ROM build |
| M2 Note, Android 9 / Linux 3.18 | Full 2 October userdebug ROM published; archive, signature, native boot and OTA checks passed | Verify boot and the complete hardware matrix on the exact board |
| U10 / U20, Android 9 / Linux 3.18 | Full 5 October userdebug ROMs published; archive, signature, native boot, OTA and build-component checks passed | Verify boot and the complete hardware matrix on each board |
| M5s, Android 9 / Linux 3.18 | Native Yassy/FT5346 kernel selected; USB and display interface corrections prepared; full ROM build in progress | Finish the complete build, publish checked artifacts, then test on hardware |
| Other Android 11 / 13 tracks | Device configuration and compatibility sources published | Complete builds and device testing |

The MX6, M5c and L681 hardware observations above retain their 29 September
baseline; they do not validate the new M2 Note, U10 or U20 downloads.

Hardware observations can come from newer development images than the source
revisions listed in the index. A compiled object or kernel is not a tested phone
image. The source repositories contain development work and may require additional
kernel, vendor and common-tree inputs. Downloadable releases are listed separately in
[remeizu-releases](https://github.com/nomorecoolnicknames/remeizu-releases/releases).

Component-level implementation and test status is documented in the
[M5s kernel README](https://github.com/nomorecoolnicknames/mtk-t-alps-release-q0-kernel-4.9-lc/tree/m5s-linux-4.9#readme)
and [Thorium shared-device README](https://github.com/nomorecoolnicknames/remeizu-thorium-source/tree/lineage-16.0#readme).

## Priorities

1. Establish usable LOS16 / Android 9 baselines, then improve Android 11 and 13.
2. Share common support across MT6735/6737, MT6753 and MT6750/6755 while preserving
   board-specific PMIC, display, sensor and memory differences. MT6752, MT6797 and
   other platforms remain separate tracks.
3. Replace practical host-driver and HAL dependencies with open implementations;
   see the [component roadmap](OPEN_COMPONENTS_ROADMAP.md).
4. Bring up upstream Linux in stages: boot, storage, USB, power, then display,
   input and connectivity. Submit tested driver and board changes upstream and
   use those foundations for postmarketOS ports.
5. Expand automated builds and device regression tests. Flashing, recovery and
   hardware acceptance still need device-specific checks.

[Source repositories](SOURCE_INDEX.md) · [Build infrastructure](BUILD_INFRASTRUCTURE.md)
