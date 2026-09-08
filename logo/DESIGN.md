# Logo design

How the Cermet symbol is built and what must be kept when it is changed. The geometry below is the content of `cermet-symbol.svg`; the SVG is the source of truth and this document explains it.

## Concept

The symbol represents ceramic and metal as two distinct phases forming a single structure. Neither material disappears into the other. Both keep their identity while together they make one whole. That is the stance of the language: TypeScript and Cermet stay what they are and form one system.

The three parts of the symbol map to the concept:

| Part | What it stands for |
|---|---|
| Ceramic, the light phase | Crystalline, hard material. Three flat facets, no gradients or gloss |
| Metal, the gray phase | A single matte blue-gray face with one facet change at the bottom edge. No chrome or reflections, so that it differs from the ceramic in texture, not in shine |
| Seam, the S-curve | The most important identifying element. The curve reaches into both phases and stands for connection, interoperation, and coexistence. It is drawn in the same Ink color as the outline and reads as one continuous structural line with it |

## Construction

The canvas is 240 by 240 units (`viewBox="0 0 240 240"`), centered at (120, 120).

- **Outline.** A regular hexagon of radius 100 around the center, with vertices at the top and bottom: `M120 20 L206.6 70 L206.6 170 L120 220 L33.4 170 L33.4 70 Z`. It is stroked in Ink at width 20 with round joins. The rounded corners come from the round join of the thick stroke; they are not a separate path.
- **Seam.** One cubic curve from the upper right to the lower left: `M140 31.5 C188 72 52 168 100 208.5`, stroked in Ink at width 11 with round caps. It is point-symmetric about the center (C2 symmetry), so it always passes through the center and neither phase wraps around the other.
- **Phases.** Each phase is one closed path made of hexagon edges plus the seam. No clip masks are used, so no hairline appears along the seam and the file stays editable in Illustrator or Figma.
  - Ceramic: `M140 31.5 L120 20 L33.4 70 L33.4 170 L120 220 L100 208.5 C52 168 188 72 140 31.5 Z` filled with `#F7F5F1`, with three facets on top: `M120 20 L33.4 70 L66 140 Z` (`#FCFBF8`), `M33.4 70 L33.4 170 L66 140 Z` (`#EFEBE4`), `M66 140 L33.4 170 L100 208.5 Z` (`#E4E0D8`). The facets are planes meeting at ridges; when the symbol is reduced to one color they disappear and the silhouette stays.
  - Metal: `M140 31.5 C188 72 52 168 100 208.5 L120 220 L206.6 170 L206.6 70 Z` filled with `#909BAA`, with one facet at the bottom: `M206.6 170 L120 220 L100 208.5 Z` (`#87919F`).
- **Drawing order.** Ceramic body, ceramic facets, metal body, metal facet, seam stroke, outline stroke.

## Variants

| Variant | Construction |
|---|---|
| Full color (`cermet-symbol.svg`) | As above |
| On dark (`cermet-symbol-dark.svg`) | Same geometry. Outline and seam in `#F7F5F1`. Ceramic facets become `#151C26` `#1F2836` `#242D3D`, metal becomes `#8B96A5` / `#7C8798` |
| Mono (`cermet-symbol-mono.svg`) | Same geometry in `currentColor`. Facets removed, phases kept as silhouette |
| Line (`cermet-symbol-line.svg`) | Outline and seam only, in `currentColor` |
| Lockup (`cermet-lockup*.svg`) | Symbol at the left, wordmark "Cermet" to the right, `viewBox="0 0 720 240"` |

## Principles to keep

- The two phases stay clearly separate and keep roughly equal area.
- Neither phase looks subordinate to the other.
- The S-curve seam is the main identifying element. Do not straighten, thin, or move it off center.
- The basic shape must hold in one color.
- The silhouette must be recognizable at small sizes.
- No 3D rendering, no gloss, no gradients.

## Sizes

- Symbol: designed to read at 48 px, 28 px, and 16 px. Below 24 px prefer the line variant or the favicon set.
- Lockup: minimum 24 px in height (README, web, social images).

## Wordmark

The wordmark is set in Poppins SemiBold (600) with a letter spacing of about -0.024 em, in Ink. It is a provisional setting in live text. Before print or distribution where fonts cannot be relied on, convert it to outlines, or draw dedicated lettering.

Poppins is published by the Indian Type Foundry under the SIL Open Font License 1.1, which allows use in logos and wordmarks and in commercial work. The fallbacks named in the SVG (Century Gothic, Futura, Verdana) are only used when Poppins is absent and are not distributed here.
