# Source repositories

Updated 6 October 2026. Android 9 uses LineageOS 16.0, Android 11 uses 18.1,
and Android 13 uses 20. Device trees require the matching Android, vendor,
common-tree and kernel inputs. These branches contain development sources;
see [device status](PROJECT_STATUS.md) for tested functionality.

Branch links follow ongoing work. Commit links identify the revision checked
for this index.

## Sources for current LOS16 builds

| Device | Branch | Checked revision | Use |
|---|---|---|---|
| M2 Note device | [lineage-16.0](https://github.com/nomorecoolnicknames/android_device_meizu_m2note-source/tree/lineage-16.0) | [d912799658a2](https://github.com/nomorecoolnicknames/android_device_meizu_m2note-source/commit/d912799658a29280b97f30c9f881abdad6b1dfab) | Current native-kernel selection and full-ROM build notes |
| M2 Note | [m2note-3.18-native](https://github.com/ReMeizu/android_kernel_meizu_mt6753/tree/m2note-3.18-native) | [be24834072fc](https://github.com/ReMeizu/android_kernel_meizu_mt6753/commit/be24834072fcafa234e61092b7f8b6a0f60a5b78) | Corresponding kernel source for the 2 October experimental ROM |
| U10 kernel | [u10-3.18](https://github.com/ReMeizu/android_kernel_meizu_mt675x/tree/u10-3.18) | [efeee9b5883c](https://github.com/ReMeizu/android_kernel_meizu_mt675x/commit/efeee9b5883c7f1e11904ce4ae076e5a7aaa2b2a) | Corresponding kernel code for the 5 October experimental ROM |
| U20 kernel | [u20-3.18](https://github.com/ReMeizu/android_kernel_meizu_mt675x/tree/u20-3.18) | [b86c36b01ef0](https://github.com/ReMeizu/android_kernel_meizu_mt675x/commit/b86c36b01ef08399f064cd2f60cb8fcf6d0b164c) | Corresponding kernel code for the 5 October experimental ROM |
| M5s device | [lineage-16.0](https://github.com/nomorecoolnicknames/android_device_meizu_m5s/tree/lineage-16.0) | [a2e280f6b39c](https://github.com/nomorecoolnicknames/android_device_meizu_m5s/commit/a2e280f6b39c3f7e9bf6c0d548e770247d4219b7) | Native-kernel, USB and display compatibility updates; full ROM pending |
| M5s | [m5s-3.18-native](https://github.com/ReMeizu/android_kernel_meizu_mt6753/tree/m5s-3.18-native) | [6a4373fd09b7](https://github.com/ReMeizu/android_kernel_meizu_mt6753/commit/6a4373fd09b75f1ca4025a9311a2c5b97cb810f6) | Selected kernel for the LOS16 build in progress; no complete ROM release yet |

Published code and successful compilation do not establish hardware operation.
Complete-ROM prereleases and checksum files are available separately in
[ReMeizu releases](https://github.com/nomorecoolnicknames/remeizu-releases/releases).

## Earlier source tracks

The following revisions were checked on 29 September 2026. They remain useful
references; a historical device or kernel snapshot does not reproduce a newer
ROM without its matching inputs.

| Device / track | Branch | Commit | Contents |
|---|---|---|---|
| M5c / Android 9 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m5c/tree/lineage-16.0) | [9f4e7324ca9d](https://github.com/nomorecoolnicknames/android_device_meizu_m5c/commit/9f4e7324ca9d73146d2ea91781647a1b90462c91) | Device tree |
| M5c / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m5c/tree/lineage-18.1) | [3d5b8bad0a83](https://github.com/nomorecoolnicknames/android_device_meizu_m5c/commit/3d5b8bad0a838e849fef7fcec63483da33bba353) | Device tree |
| M5c / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m5c/tree/lineage-20-treble) | [3f14407092a9](https://github.com/nomorecoolnicknames/android_device_meizu_m5c/commit/3f14407092a9fe1ca3efbd611d42a8bb51c6f2bc) | Device tree |
| M6T / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m6t-source/tree/lineage-18.1) | [8a45a28baa26](https://github.com/nomorecoolnicknames/android_device_meizu_m6t-source/commit/8a45a28baa26d0e49bbfd4443c0f2b0d8c9d70b3) | Device tree |
| M6T / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m6t-source/tree/lineage-20.0) | [c19f59d1457a](https://github.com/nomorecoolnicknames/android_device_meizu_m6t-source/commit/c19f59d1457aa646a0e5a71bd5d3dc37a62763f4) | Device tree |
| M6T / Android 9 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m6t-source/tree/lineage-16.0) | [5a1c776e22ec](https://github.com/nomorecoolnicknames/android_device_meizu_m6t-source/commit/5a1c776e22ece3298bb8c731e8ce2918329813b3) | Device tree |
| M3 Note L681 / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_l681-source/tree/lineage-18.1) | [414fac0b54ef](https://github.com/nomorecoolnicknames/android_device_meizu_l681-source/commit/414fac0b54ef18c960a7988125ce074b6b936b1b) | Device tree |
| M3 Note L681 / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_l681-source/tree/lineage-20.0) | [03dba85c96d9](https://github.com/nomorecoolnicknames/android_device_meizu_l681-source/commit/03dba85c96d9ec1103c4aa01d8059e59deb0c081) | Device tree |
| M3 Note L681 / Android 9 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_l681-source/tree/lineage-16.0) | [8047ff4702f1](https://github.com/nomorecoolnicknames/android_device_meizu_l681-source/commit/8047ff4702f1d4650bb07b49197b6f31271a495b) | Device tree |
| M3 Note M681 / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m681-source/tree/lineage-18.1) | [b0935025e50c](https://github.com/nomorecoolnicknames/android_device_meizu_m681-source/commit/b0935025e50c6df87cece471540c2450f807c0df) | Device tree |
| M3 Note M681 / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m681-source/tree/lineage-20.0) | [0cb19dc5422e](https://github.com/nomorecoolnicknames/android_device_meizu_m681-source/commit/0cb19dc5422e1e91ff5b5c4c8ef6afb07cd6eee2) | Device tree |
| M3 Note M681 / Android 9 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m681-source/tree/lineage-16.0) | [1c3c2a7cee9d](https://github.com/nomorecoolnicknames/android_device_meizu_m681-source/commit/1c3c2a7cee9d413967724d2eef9b94e92894e93a) | Device tree |
| M6 / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m6-source/tree/lineage-18.1) | [ae3154b9a5f2](https://github.com/nomorecoolnicknames/android_device_meizu_m6-source/commit/ae3154b9a5f2f5b17a1584cca1c507c9478fbf52) | Device tree |
| M6 / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m6-source/tree/lineage-20.0) | [61dc85effe97](https://github.com/nomorecoolnicknames/android_device_meizu_m6-source/commit/61dc85effe97914441418c46d035bb24c9d8a331) | Device tree |
| M6 / Android 9 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m6-source/tree/lineage-16.0) | [b31f1449e251](https://github.com/nomorecoolnicknames/android_device_meizu_m6-source/commit/b31f1449e25129810cf9b6d239d8b466c4ec6f55) | Device tree |
| Thorium / Android 9 | [source](https://github.com/nomorecoolnicknames/remeizu-thorium-source/tree/lineage-16.0) | [17f78289bb65](https://github.com/nomorecoolnicknames/remeizu-thorium-source/commit/17f78289bb6528bb5e4d3ba14d098e8a8dfdf0b1) | Shared device support |
| M5s / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m5s/tree/lineage-18.1) | [c72cb81949aa](https://github.com/nomorecoolnicknames/android_device_meizu_m5s/commit/c72cb81949aab2a3e1a91e818bc1ced24779245f) | Device tree |
| M5s / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m5s/tree/lineage-20.0) | [ff5870bae98e](https://github.com/nomorecoolnicknames/android_device_meizu_m5s/commit/ff5870bae98ef9e194bf18c2ef471fddebe044fc) | Device tree |
| M2 Note / Android 11 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m2note-source/tree/lineage-18.1) | [48da714e8528](https://github.com/nomorecoolnicknames/android_device_meizu_m2note-source/commit/48da714e85280ecd6de4ef6c31b6995581b62704) | Device tree |
| M2 Note / Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m2note-source/tree/lineage-20.0) | [7eebec3b4d15](https://github.com/nomorecoolnicknames/android_device_meizu_m2note-source/commit/7eebec3b4d152e0151e4bff19e66d77711805134) | Device tree |
| M5s / Linux 4.9 | [source](https://github.com/nomorecoolnicknames/mtk-t-alps-release-q0-kernel-4.9-lc/tree/m5s-linux-4.9) | [c9b8e1b4a307](https://github.com/nomorecoolnicknames/mtk-t-alps-release-q0-kernel-4.9-lc/commit/c9b8e1b4a307a5ec3d4c6f83b74fe04f85e7ceb0) | Kernel and M5s board support |
| U10 / Linux 3.18 | [source](https://github.com/nomorecoolnicknames/android_kernel_meizu_m6/tree/u10-linux-3.18-patches) | [3009821156c6](https://github.com/nomorecoolnicknames/android_kernel_meizu_m6/commit/3009821156c60564fd024ea46a32a1cc62314f16) | Board and driver patch series |
| U20 / Linux 3.18 | [source](https://github.com/nomorecoolnicknames/android_kernel_meizu_m6/tree/u20-linux-3.18) | [f99cc7eeb92b](https://github.com/nomorecoolnicknames/android_kernel_meizu_m6/commit/f99cc7eeb92b24230ab8f23c32e2f21fd43e050f) | Initial board resources |
| MX6 / M95 Android 13 | [source](https://github.com/nomorecoolnicknames/android_device_meizu_m95-source/tree/lineage-20.0) | [983deb2fe675](https://github.com/nomorecoolnicknames/android_device_meizu_m95-source/commit/983deb2fe675844e09faef0dc32445271d7f63ab) | Native LineageOS 20 device tree |
| MX6 / M95 kernel 3.18.22 | [source](https://github.com/nomorecoolnicknames/android_kernel_meizu_m95/tree/lineage-20.0) | [03ac08617bc2](https://github.com/nomorecoolnicknames/android_kernel_meizu_m95/commit/03ac08617bc2de148da79ab8d13bcc15b76d9245) | Kernel for native Android 13 |

The earlier U10 snapshot is a patch series with application prerequisites in its
repository; the earlier U20 snapshot contains initial board resources. Those
historical snapshots do not describe the newer complete LOS16 build results. Build infrastructure is maintained separately in
[ReMeizu/build-infra](https://github.com/ReMeizu/build-infra).
