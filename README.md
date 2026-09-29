# ReMeizu

Custom LineageOS firmware for older Meizu phones (bring-up). Live site via GitHub Pages.

Unofficial, not affiliated with Meizu.

## Project status

The Russian and English device pages were refreshed on 29 September 2026.
Hardware observations, compilation results and source preparation have separate
labels. Android 13 has booted on M5c and MX6; this does not imply a stable
Android 9/11/13 release across the fleet. M6's existing Android 8.1 release link
is retained. Other source tracks do not offer an unverified ROM download.

- [Published source index and exact revisions](https://github.com/nomorecoolnicknames/remeizu/blob/codex/progress-and-roadmap-20260929/SOURCE_INDEX.md)
- [Project progress](https://github.com/nomorecoolnicknames/remeizu/blob/codex/progress-and-roadmap-20260929/PROJECT_STATUS.md)
- [MX6 runtime scope](https://github.com/nomorecoolnicknames/android_device_meizu_m95-source/blob/827e1083db4dfc961b26641fc77a052ac66f3872/RUNTIME_SUMMARY.json)
- [M5s kernel compile evidence](https://github.com/nomorecoolnicknames/mtk-t-alps-release-q0-kernel-4.9-lc/blob/e2a0b2e51b87ce7aca65775d92c9269df8f27201/Documentation/remeizu-m5s/cloud-a4-compile-proof.json)

M5c, L681 and the cloud-port entries use the maintainers' 29 September status
snapshot. A component that starts, or an object that compiles, is not listed as
fully working on hardware. Earlier third-party M2 resources are identified as
historical references. The separate M1721 Linux track links its own repositories.

## Editing and publishing

Edit the device data and localized copy in `ReMeizu.dc.html`. `support.js` is the
generated page runtime and is unchanged by this content refresh. `index.html`
redirects to the device catalogue. GitHub Pages serves the root of `main`.

Preview with `python -m http.server 8765`, then check both languages, device
routes, source links and chipset filters before publishing. Keep source-only
entries distinct from downloadable, device-tested releases.
