# ReMeizu

LineageOS and Linux development for older Meizu phones, with shared chipset
support and device-specific ports.

[Project website](https://nomorecoolnicknames.github.io/remeizu/ReMeizu.dc.html) ·
[Device status](PROJECT_STATUS.md) · [Source repositories](SOURCE_INDEX.md) ·
[Open-component roadmap](OPEN_COMPONENTS_ROADMAP.md) · [Build infrastructure](BUILD_INFRASTRUCTURE.md)

Maintained by [Vladislav](https://github.com/nomorecoolnicknames), with
[M5c contributions from Dekompilyator](https://github.com/Dekompilyator).
Updates: [Telegram](https://t.me/remeizu).

## Editing the site

Device data and translations live in `ReMeizu.dc.html`; `support.js` provides
the generated page runtime. `index.html` redirects to the device catalogue.
GitHub Pages serves the root of `main`.

Preview with `python -m http.server 8765`, then check both languages, device
routes, source links and chipset filters. Keep development source links separate
from downloadable releases that have been tested on hardware.

## Image credit

The MX6 product image is from the
[GSMArena Meizu MX6 gallery](https://www.gsmarena.com/meizu_mx6-pictures-8078.php).

Unofficial; not affiliated with Meizu, LineageOS or postmarketOS.
