# cermet-lang/brand

This repository holds the visual identity of the Cermet programming language: the logo, the color palette, the naming, and the rules for using them. It is written in English. Japanese versions of a document, when kept, sit next to it with the suffix `.ja.md`.

## What belongs here

- The logo (`logo/`), with SVG as the source of truth and PNG as rendered output.
- The color palette (`colors/`) in three forms that must agree: `colors.md`, `colors.json`, `colors.css`.
- Favicons rendered from the symbol (`favicon/`).
- The name and how to write it (`NAMING.md`).
- The design concept and construction rules of the logo (`logo/DESIGN.md`).

What does not belong here: the language specification (`cermet-lang/spec`), the compiler, documentation for users of the language. This repository explains how Cermet looks and how it is called, not how it works.

## Rules

- **SVG is the source.** Change `logo/*.svg` first, then re-render the PNGs and favicons. Never edit a PNG by hand.
- **Colors live in the SVG.** When a color changes, change it in the SVG, then update `colors/colors.md`, `colors/colors.json`, and `colors/colors.css` in the same commit. The three files list the same tokens with the same hex values.
- **Keep the variants in sync.** `cermet-symbol.svg`, `cermet-symbol-dark.svg`, `cermet-symbol-mono.svg`, and `cermet-symbol-line.svg` share the same geometry. A change to the shape is applied to all four, and to both lockups.
- **Do not change the geometry casually.** The hexagon, the S-curve, and the facet lines are the identity. A change to them is a redesign and needs a note in the commit message explaining why.
- **The wordmark uses live text.** `cermet-lockup*.svg` sets "Cermet" in Poppins 600. Rendering depends on the font being available. If a fixed rendering is needed (print, embedding where fonts cannot be trusted), export a copy with the text converted to outlines and mark it as such in the file name.
- **Naming.** Write "Cermet" for the language, `cermet` for identifiers, `.cerm` for the extension, `cermet-lang` for the GitHub organization. Never "Cermet Language" as a proper noun. The first mention in a document may say "the Cermet programming language" to disambiguate from the material.
- Do not use em dashes in prose. Use a comma, a period, or parentheses.

## Rendering

Favicons and PNGs are rendered with ImageMagick from the SVG:

```
magick -background none logo/cermet-symbol.svg -resize 512x512 favicon/favicon-512.png
magick favicon/favicon-16.png favicon/favicon-32.png favicon/favicon-48.png favicon/favicon.ico
```

Re-render everything in `favicon/` and `logo/png/` after any change to the SVG.

## git

- Commit messages are one line in English, imperative mood ("Add dark lockup", "Adjust metal shadow"). No body, no `Co-Authored-By` or other trailers.
- Do not commit or push unless asked. Add files by path, not with `git add .`.
