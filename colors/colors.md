# Colors

The palette is taken from the logo SVG files, which are the reference. `colors.json` and `colors.css` list the same tokens.

## Palette

| Token | Hex | Role |
|---|---|---|
| `ink` | `#1C2431` | Outline of the symbol, the wordmark, body text on light backgrounds, dark backgrounds |
| `ceramic-100` | `#FCFBF8` | Ceramic phase, brightest facet |
| `ceramic-200` | `#F7F5F1` | Ceramic phase, main facet. Also the light page background (`paper`) |
| `ceramic-300` | `#EFEBE4` | Ceramic phase, mid facet |
| `ceramic-400` | `#E4E0D8` | Ceramic phase, shadow facet |
| `metal-400` | `#909BAA` | Metal phase, main facet on light backgrounds |
| `metal-500` | `#87919F` | Metal phase, shadow facet on light backgrounds |
| `metal-dark-400` | `#8B96A5` | Metal phase, main facet on dark backgrounds |
| `metal-dark-500` | `#7C8798` | Metal phase, shadow facet on dark backgrounds |
| `ink-700` | `#242D3D` | Dark variant, brightest facet of the left half |
| `ink-800` | `#1F2836` | Dark variant, mid facet of the left half |
| `ink-900` | `#151C26` | Dark variant, shadow facet of the left half |
| `paper` | `#F7F5F1` | Light background. Same value as `ceramic-200` |

## Combinations

| Background | Symbol | Text |
|---|---|---|
| `paper` or white | `cermet-symbol.svg` | `ink` |
| `ink` | `cermet-symbol-dark.svg` | `ceramic-200` |
| Any single color | `cermet-symbol-mono.svg` or `cermet-symbol-line.svg` in a contrasting color | same color |

## Typography

The wordmark uses Poppins SemiBold (600), letter spacing about -0.024 em, in `ink`. Poppins is published by the Indian Type Foundry under the SIL Open Font License 1.1 and may be used in logos and commercial work. No font file is distributed in this repository.

## Contrast

`ink` on `paper` has a contrast ratio of about 14:1 and passes WCAG AAA for text of any size. `metal-400` on `paper` is decorative only and is not used for text.
