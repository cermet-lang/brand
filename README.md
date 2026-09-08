# Cermet brand

Visual identity of the Cermet programming language: logo, colors, naming, and usage guidelines.

Cermet is a programming language that lives on the same module graph as TypeScript and TSX. TypeScript code imports Cermet modules, and Cermet modules import TypeScript, JavaScript, and npm packages, without a build step in between. The name comes from the composite material: a ceramic phase and a metal phase that keep their own properties while forming one material. The logo shows exactly that.

## What is in this repository

| Path | Contents |
|---|---|
| `logo/` | The logo. SVG files are the source of truth. `logo/png/` holds rendered PNGs at 1024 px. `logo/DESIGN.md` explains the concept and the construction |
| `colors/` | The color palette as a document, as JSON tokens, and as CSS custom properties |
| `favicon/` | Favicons rendered from `logo/cermet-symbol.svg` |
| `NAMING.md` | The name, how to write it, and why it was chosen |
| `AGENTS.md` | How this repository is maintained |

## Logo

The symbol is a hexagon split by an S-curve. The left half is the ceramic phase (warm off-white facets), the right half is the metal phase (cool gray facets), and the outline in Ink holds them together as one shape.

| File | Use it when |
|---|---|
| `logo/cermet-symbol.svg` | The symbol on a light background. Default |
| `logo/cermet-symbol-dark.svg` | The symbol on a dark background. Facets and outline are inverted for contrast |
| `logo/cermet-symbol-mono.svg` | One color only (`currentColor`). Print, stamps, embossing, places where the palette is not available |
| `logo/cermet-symbol-line.svg` | Outline only (`currentColor`). Small sizes on busy backgrounds, icon fonts |
| `logo/cermet-lockup.svg` | Symbol and wordmark side by side, light background |
| `logo/cermet-lockup-dark.svg` | Symbol and wordmark, dark background |
| `logo/png/cermet-symbol-1024.png` | Rendered symbol, transparent background |
| `logo/png/cermet-symbol-dark-1024.png` | Rendered symbol on the dark Ink background |
| `logo/png/cermet-symbol-1024-on-white.png` | Rendered symbol on white |

Rules for using the logo:

- Use the SVG files unchanged. Do not recolor, rotate, skew, add effects, or redraw the S-curve.
- Keep clear space around the symbol of at least one quarter of its height on every side.
- Do not render the symbol smaller than 16 px. Below 24 px prefer `cermet-symbol-line.svg` or the favicon set.
- On photographs or gradients use the mono or line variant in a single color that has enough contrast.
- The wordmark is set in Poppins SemiBold (600) with tight letter spacing. Poppins is an open font (SIL Open Font License 1.1) and may be used in logos and commercial work. `cermet-lockup.svg` uses live text and falls back to Century Gothic, Futura, or Verdana when Poppins is not installed. Convert the text to outlines before sending the lockup to print.
- The word is written "Cermet" in prose and `cermet` in identifiers (CLI, package names, the `.cerm` extension). Do not write "Cermet Language" as a proper noun; see `NAMING.md`.

## Colors

Hex values are taken from the SVG files and are the reference. See `colors/colors.md` for the full palette with roles, `colors/colors.json` for tokens, and `colors/colors.css` for CSS custom properties.

| Role | Hex |
|---|---|
| Ink (outline, wordmark, text on light) | `#1C2431` |
| Ceramic (highlight to shadow) | `#FCFBF8` `#F7F5F1` `#EFEBE4` `#E4E0D8` |
| Metal (light, shadow) | `#909BAA` `#87919F` |
| Metal on dark backgrounds | `#8B96A5` `#7C8798` |
| Dark facets (dark variant) | `#151C26` `#1F2836` `#242D3D` |
| Paper (light background) | `#F7F5F1` |

## Favicons

`favicon/` contains `favicon.svg`, `favicon.ico` (16, 32, 48 px), `favicon-16.png`, `favicon-32.png`, `favicon-48.png`, `favicon-512.png`, and `apple-touch-icon.png` (180 px). They are rendered from `logo/cermet-symbol.svg` with ImageMagick; see `AGENTS.md` for the command.

## License

The contents of this repository are licensed under the Creative Commons Attribution-NoDerivatives 4.0 International License (CC BY-ND 4.0). You may copy and redistribute the logo and the palette, including for commercial use, as long as you give credit and do not distribute modified versions. Rendering the SVG at a different size, or choosing one of the provided variants, is not a modification. See `LICENSE`.
