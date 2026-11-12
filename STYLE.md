# HamsterProjekt style

HamsterProjekt keeps the look of the original Hamster Projekt, the hamster
wheel on its stand, and redraws it with the KDE
[Breeze](https://develop.kde.org/hig/) palette so it sits well next to
Plasma 6.

Open [`style/index.html`](style/index.html) in a browser to see everything
below in light and dark.

## Logo

<img src="assets/logo/hamsterprojekt.svg" width="96" height="96" alt="HamsterProjekt logo">

The wheel from the original Tango icon, flattened:

- a **Plasma blue** rim (`#3daee9` to `#1d82c8`) with light rungs,
- a long **icon blue** spoke (`#1d99f3`) and a short **charcoal** spoke, so
  the wheel also reads as a clock,
- a **charcoal** hub and stand (`#31363b`).

| File | Use |
|---|---|
| [`assets/logo/hamsterprojekt.svg`](assets/logo/hamsterprojekt.svg) | Application icon, 48 px grid, scales freely |
| [`assets/logo/hamsterprojekt-symbolic.svg`](assets/logo/hamsterprojekt-symbolic.svg) | Monochrome 16 px icon for menus and panels |
| [`assets/avatar.svg`](assets/avatar.svg), [`assets/avatar.png`](assets/avatar.png) | Organization avatar, 512 px |
| [`assets/banner-light.svg`](assets/banner-light.svg), [`assets/banner-dark.svg`](assets/banner-dark.svg) | Header for the organization page |

Leave space around the logo of at least a quarter of its width, and do not
recolour, stretch or rotate it.

## Symbolic icons

<img src="assets/icons/hamster-tracking-symbolic.svg" width="32" height="32" alt="Tracking">
<img src="assets/icons/hamster-idle-symbolic.svg" width="32" height="32" alt="Idle">

16 px icons drawn the KDE way: fills only (no masks or filters, so Qt's SVG
renderer handles them), and colours taken from the
`current-color-scheme` stylesheet. Plasma recolours `ColorScheme-Text` to
match the panel; elsewhere they show in Breeze's dark grey.

| File | State |
|---|---|
| [`hamster-tracking-symbolic.svg`](assets/icons/hamster-tracking-symbolic.svg) | Tracking: spokes in `ColorScheme-PositiveText` (green) |
| [`hamster-idle-symbolic.svg`](assets/icons/hamster-idle-symbolic.svg) | Not tracking: the whole glyph at 50 % opacity |

## Feature icons

<img src="assets/features/markdown.svg" width="32" alt=""> <img src="assets/features/service.svg" width="32" alt="">
<img src="assets/features/plasma.svg" width="32" alt=""> <img src="assets/features/install.svg" width="32" alt="">
<img src="assets/features/compatible.svg" width="32" alt=""> <img src="assets/features/upstream.svg" width="32" alt="">

Rounded tiles (radius 10 on a 48 px grid) with a white line glyph, one
Breeze colour each. They are for READMEs and web pages, not for the
desktop: `markdown`, `service`, `plasma`, `install`, `compatible`,
`upstream`.

## Colours

| Name | Hex | Use |
|---|---|---|
| Plasma blue | `#3daee9` | Accent, links on dark, primary buttons |
| Icon blue | `#1d99f3` | The wheel's spoke, the "Projekt" in the wordmark |
| Rim blue | `#1d82c8` | Shadows and pressed states of blue |
| Charcoal | `#31363b` | Stand, hub, dark surfaces |
| Shade | `#232629` | Text on light |
| Paper | `#fcfcfc` | Text on dark, light surfaces |
| Cloud | `#eff0f1` | Light window background |
| Positive | `#27ae60` | Tracking |
| Neutral | `#f67400` | Warnings |
| Negative | `#da4453` | Errors, overlapping facts |

Categories get these colours in order, as in the totals bar under the
day's facts: `#3daee9`, `#2ecc71`, `#f67400`, `#9b59b6`, `#fdbc4b`,
`#1abc9c`, `#da4453`, `#7f8c8d`.

## Type

Noto Sans, the Plasma default, at 10 pt; Hack for code. The wordmark is
"Hamster" in bold text colour followed by "Projekt" in icon blue, with no
space.

## Stylesheet

[`style/hamsterprojekt.css`](style/hamsterprojekt.css) holds the colours,
spacing and type above as `--hp-*` custom properties, plus a few
components with `hp-` classes:

- `hp-header`, `hp-wordmark`: a page header with the logo
- `hp-card`, `hp-button` (`is-primary`), `hp-status` (`is-tracking`)
- `hp-tag`: Hamster's tag chips
- `hp-facts`: the list of facts for a day
- `hp-totals`, `hp-legend`: the share of the day per category
- `hp-features`, `hp-feature`: a grid of feature icons with text

It follows the system's light or dark setting; force one with
`<html data-theme="light">` or `data-theme="dark"`. Reports print without
the header and buttons.

## License

The icons, banners and stylesheet are licensed under the GNU GPL v3, like
the rest of HamsterProjekt. The logo is a redrawing of the original Hamster
icon.
