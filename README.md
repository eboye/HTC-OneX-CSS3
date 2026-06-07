HTC-One-X-CSS3
==============

The amazing HTC One X phone drawn purely in CSS. The only two images are the
GIF used as the display boot animation and a noise texture for subtle grain on
the device body — everything else is CSS.

Everything is sized in `em`, so the device scales cleanly, and the logo and
icons are a custom vector font, so they stay crisp on high-DPI displays at any
size.

Originally a 2012 weekend project, modernized in 2026 (see below).

Demo
-----------
https://eboye.github.io/HTC-OneX-CSS3/

2026 modernization
-----------
The original CSS3 markup was brought up to date with current web standards
while keeping the look identical on desktop:

- **Native CSS nesting** mirroring the markup hierarchy.
- **Logical properties** (`inline-size`, `block-size`, `inset-*`, `margin-block-*`).
- **`color-mix()`** to derive the warm/cool glow shadows from base accent hues.
- **`light-dark()` + `color-scheme`** for `prefers-color-scheme` support — the
  iconic dark "studio" look is the default, with a tuned light variant for
  users whose OS prefers light.
- **Responsive layout** — below 700px the page stacks into a single column with
  the title above the phone; the desktop side-by-side composition is unchanged.
- **`prefers-reduced-motion`** support — keeps the visual emphasis, drops the
  movement.
- Subtle **hover** interaction: the device lifts and its glow intensifies
  (with the cast shadow responding via `:has()`).
- Modern `woff2` font with `font-display`; the dead IE-only `.eot`/`.svg` font
  formats and all IE / Chrome Frame markup were removed.
- Accessibility fixes: `alt` text, `aria-label`s on the icon-font navigation and
  logo, valid markup, and a proper `viewport` meta.

Browser support
-----------
Targets evergreen browsers (Chrome, Firefox, Safari, Edge). The modern CSS
features used — nesting, `color-mix()`, `light-dark()`, logical properties — are
Baseline as of 2024/2025.

Deployment
-----------
The live demo is served from the `gh-pages` branch. A GitHub Actions workflow
(`.github/workflows/sync-gh-pages.yml`) mirrors `master` to `gh-pages` on every
push, so the demo always reflects `master` — treat `master` as the source of
truth and don't commit directly to `gh-pages`.

Found a bug?
-----------
Please open an issue: https://github.com/eboye/HTC-OneX-CSS3/issues

Copyright and license
-----------

Copyright 2012 SrboDroid.

Licensed under the Creative Commons License, Version 3.0

You must attribute the work in the manner specified by the author or licensor (but not in any way that suggests that they endorse you or your use of the work).

You may not use this work for commercial purposes.

If you alter, transform, or build upon this work, you may distribute the resulting work only under the same or similar license to this one.

More about licence:

http://creativecommons.org/licenses/by-nc-sa/3.0/deed.en_US
