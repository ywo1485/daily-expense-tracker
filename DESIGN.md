# Design

The visual system for Daily Spend, recorded from the built page (`index.html`). Product truth lives in [PRODUCT.md](PRODUCT.md).

## World

A loyalty stamp card. White cards outlined in plum ink sit on a blush ground, and every day logged is a pastel rubber stamp on the month's card. The palette is "Pastel Mix": each day's stamp takes the pastel of the category that day spent most on.

## Colour

| Token | Light | Dark | Job |
|---|---|---|---|
| `--bg` | `#FBF3F7` | `#211B2A` | Page ground |
| `--surface` | `#FFFFFF` | `#2B2437` | Cards, fields, buttons at rest |
| `--ink` | `#3D3350` | `#F3ECF8` | Text |
| `--muted` | `#6F6480` | `#B0A5BF` | Secondary text, unstamped circles |
| `--rule` | `#3D3350` | `#9A8FAE` | The 2px outline on cards and controls |
| `--line` | `#E6DAE6` | `#43394F` | Dashed dividers inside a card |
| `--accent` | `#CDB7F6` | same | Primary button |
| `--accent-deep` | `#8E6FD0` | `#B79CF0` | Focus ring, today's ring, link underline |
| `--mint` | `#BFEBD0` | same | "Fed" state, tummy stamps, budget fill |
| `--warn` | `#B8405F` | `#FF9DB5` | Errors, over budget, delete |
| `--on-pastel` | `#3D3350` | same | Text on any pastel fill |

Category pastels, in display order: `#D9C8F5` `#FFC8DD` `#BFEBD0` `#BDE0FE` `#FFD6BA` `#FFF0B3` `#F9BCC8` `#C9D1FA` `#F3C4F0` `#BEEDEA` `#E4DEEA`. A pastel is only ever a fill behind plum text; it is never text on white.

## Type

Rubik, weights 500, 700 and 900. One family for everything.

| Role | Size / weight |
|---|---|
| Amount field | `clamp(56px, 19vw, 76px)` / 900, tracking -0.03em |
| Figure (budget) | 34px / 900 |
| Page title | 22px / 900 |
| Card heading | 18px / 900 |
| Body | 16px / 500 |
| Secondary | 14px or 13px / 500 to 700 |
| Micro labels | 12px / 700 |

Numbers that line up use tabular figures.

## Shape and depth

- Cards: 2px `--rule` outline, 14px radius, 16px padding, no shadow.
- Controls: pills (999px radius) with the same 2px outline. Text fields use a 12px radius.
- Depth is flat. Nothing has a drop shadow; emphasis comes from fill and outline.

## Components

- **Stamp**: a pastel disc with a 2px outline and an inner ring, rotated a few degrees. Used for logged days, earned badges and tummy marks.
- **Unstamped circle**: dashed outline, no fill. A day filled in later is a dashed circle with a pale tint. Today has a 3px `--accent-deep` ring.
- **Category pill**: white with a small colour dot at rest; filled with its pastel and tilted when selected. Five show by default and "More" reveals the rest.
- **Primary button**: lilac pill, 900 weight, 50px tall. Secondary buttons are white pills.
- **Bar**: 14px pill with a 2px outline; fill is mint, or `--warn` when over budget.

## Motion

One authored moment: logging today thumps a stamp onto today's circle while the panda eats. Easing is `cubic-bezier(.16, 1, .3, 1)`. Confetti fires only on a level-up. All motion is removed under `prefers-reduced-motion`.

## Layout

One column up to 520px wide on phones; two equal columns above 900px (log and entries on the left; stamp card, budget and level on the right). Spacing steps: 6, 8, 10, 14, 16, 24px.
