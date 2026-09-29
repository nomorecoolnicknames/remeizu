# ReMeizu

Custom LineageOS firmware for older Meizu phones (bring-up). Live site via GitHub Pages.

Unofficial, not affiliated with Meizu.

## Project status

The Russian and English device pages were refreshed on 29 September 2026.
Hardware observations, compilation results and source preparation have separate
labels. Android 13 has booted on M5c and MX6; this does not imply a stable
Android 9/11/13 release across the fleet. M6's existing Android 8.1 release link
is retained. Other source tracks do not offer an unverified ROM download.

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

## Device images

MX6 and M6 Note product images are from the GSMArena device galleries:

- [Meizu MX6](https://www.gsmarena.com/meizu_mx6-pictures-8078.php)
- [Meizu M6 Note](https://www.gsmarena.com/meizu_m6_note-pictures-8802.php)

Keep public pages focused on device support, downloads and source repositories.
Partner correspondence, resource requests and internal status reports belong outside this site.
