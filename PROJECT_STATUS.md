# ReMeizu — progress and roadmap

Updated 29 September 2026. ReMeizu is an independent effort to extend the useful
life of older Meizu phones through reusable chipset support, newer Android
versions and a path toward upstream Linux/postmarketOS.

The project combines practical device bring-up with work that other maintainers
can reuse: source trees, board descriptions, compatibility layers and verifiable
build results. The planning scope currently covers **17 models across six chipset
families**. That is the project scope, not a claim that all 17 devices are supported.

## Published work

**23 device/common source branches and four kernel-development/source-series
branches are public.** They contain implemented work with revision provenance.
The [source index](SOURCE_INDEX.md) lists every branch and exact published commit.

| Track | Demonstrated result | Next milestone |
|---|---|---|
| MX6 / M95, native Android 13 | LOS20 userdebug boots; LTE data and IMS registration observed in build 23 on 26 September | Validate the built incoming-IMS-call fix and newer camera ownership fix; complete camera/power/suspend acceptance |
| M5c, Android 13 / custom 4.9 | Hardware boot, visible display and touch confirmed; Wi-Fi scanning observed | Complete connectivity, audio, camera and power validation; reproducible integrated images |
| M5s, custom 4.9 A4 | Full kernel linkage and Image.gz compilation; own panel selection, storage binding and corrected display address tables verified in compiled outputs | Complete board/DTB checks, boot-image packaging and first hardware validation |
| U10, driver work | Touch/power objects compiled against the original development inputs | Complete the board port and full-kernel build; public patch series has a separate application prerequisite |
| M3s / U10 / U20, LOS16 | Product/build-graph checks succeeded for Android 9 userdebug | Kernel/vendor integration and full-ROM builds |
| M5s / M2 Note, LOS16 | Full-ROM build attempts reached framework/native compilation and produced actionable logs | M5s hit its three-hour job limit; M2 Note stopped on missing returns in libgem; neither run produced an accepted ROM |
| Android 11 / 13 device sources | Real configuration, init/HAL and compatibility work for eight device tracks | Android 11 full builds and device validation; broaden Android 13 acceptance beyond the M5c and MX6 hardware baselines |

The [M5s kernel branch](https://github.com/nomorecoolnicknames/mtk-t-alps-release-q0-kernel-4.9-lc/tree/codex/m5s-4.9-a4-source)
contains a [public compile receipt](https://github.com/nomorecoolnicknames/mtk-t-alps-release-q0-kernel-4.9-lc/blob/e2a0b2e51b87ce7aca65775d92c9269df8f27201/Documentation/remeizu-m5s/cloud-a4-compile-proof.json)
with all 11 artifact hashes. Its kernel source matches the compiled development
source plus the documented board patches; the publication is not a new build.
It does not yet provide a validated DTB/boot image or hardware result.

MX6 has native LineageOS 20 in addition to its earlier Android 13 GSI work.
The [device source](https://github.com/nomorecoolnicknames/android_device_meizu_m95-source/tree/codex/lineage-20-source-20260929)
and [kernel source](https://github.com/nomorecoolnicknames/android_kernel_meizu_m95/tree/codex/lineage-20-source-20260929)
retain filtered development history and distinguish hardware-observed build 23,
built-only build 24 and the later source fixes. The
[runtime summary](https://github.com/nomorecoolnicknames/android_device_meizu_m95-source/blob/827e1083db4dfc961b26641fc77a052ac66f3872/RUNTIME_SUMMARY.json)
records exact identities and limitations. The kernel baseline is Linux 3.18.22;
this is not a claim of mainline support or a fully stable ROM.

Source publication, compilation and hardware acceptance are tracked separately.
Device exports are not standalone complete ROMs. U10's public kernel contribution
is an unapplied patch series; U20's new public resource branch is not compiled.
Those boundaries are documented in their branch READMEs and provenance files.

## Direction

1. **Useful Android baselines.** Stabilize LOS16/Android 9 userdebug while
   developing Android 11 and 13. Share proven interfaces and thin board-specific
   configurations instead of repeating each port from scratch.
2. **Reusable chipset support.** Consolidate MT6735/6737, MT6753 and MT6750/6755
   work while retaining real board, PMIC, sensor and ABI differences. MT6752,
   MT6797 and Qualcomm MSM8953 remain distinct tracks.
3. **Open components.** Inventory remaining dependencies, reuse upstream code,
   and implement openly licensed host drivers/HALs where practical. Small,
   testable components come first; graphics and camera are staged larger efforts.
   See the [component roadmap](OPEN_COMPONENTS_ROADMAP.md).
4. **Upstream Linux and postmarketOS.** Start with verified board resources,
   boot/storage/USB and power support; submit small hardware-tested improvements
   to the appropriate upstream projects, then develop device ports. This is a
   contribution plan, not a claim of accepted upstream support for every device.
5. **Repeatable validation.** Continue pinned source/toolchain recipes, artifact
   hashes and failure receipts; connect them to device readback and functional
   tests. The complete autonomous flash/test/repair loop is still being developed.

## A focused infrastructure pilot

The proposed OSL workload is Linux kernel cross-compilation, DTS/binding checks
and regression tests, using a separately reviewed, revision-pinned open-source
input set. Android ROM builds are outside that proposed scope. Whole inherited
vendor repositories are not presumed eligible merely because they are public.

A starting request is one serial worker with 4 vCPUs, 16 GiB RAM and 100 GiB
scratch, at most 30 jobs/month and two hours/job. This is a proposed resource
budget, not a measured minimum or currently provisioned service. The initial
pilot would measure resource use and retain reproducible results.

## Project and contact

Maintainer/contact: **Vladislav** ([nomorecoolnicknames](https://github.com/nomorecoolnicknames)).
Development is maintainer-led and AI-assisted, with M5c collaboration with
[Dekompilyator](https://github.com/Dekompilyator). Release milestones follow device
validation. No regular release cadence or external contributor/tester count is
claimed here.

- [Project repository](https://github.com/nomorecoolnicknames/remeizu)
- [Project site](https://nomorecoolnicknames.github.io/remeizu/ReMeizu.dc.html)
- [Telegram announcements](https://t.me/remeizu)
- [M6 Android 8.1 release example, published June 2026](https://github.com/nomorecoolnicknames/remeizu-releases/releases/tag/meizu_m6-lineage-15.1-20260622)

Unofficial; not affiliated with Meizu, LineageOS or postmarketOS.
