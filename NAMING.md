# The name

## Cermet

The language is called **Cermet**, pronounced like the material. The name is written "Cermet" in text of any language.

"Cermet" is a common noun for a composite material made of a **cer**amic phase and a **met**al phase. It is not a coinage of this project.

## What it means

A cermet is one material made of two phases with different properties. The two are not blended into something uniform. Each phase keeps its own nature, and together they form one material.

The language works the same way.

- TypeScript code imports Cermet modules, and Cermet imports TypeScript, JavaScript, and npm packages.
- The existing ecosystem (React, Vite, npm) is used as it is.
- TypeScript and Cermet are mixed in one codebase.
- And still, Cermet is not a dialect of TypeScript. It is a separate language with its own syntax and type system.

Things with different properties form one whole while each keeps its own nature. That is the stance of the language, coexistence rather than replacement, and the material describes it in one word.

## How to write it

| Context | Write |
|---|---|
| The language, in prose | Cermet |
| First mention, when the material could be meant | the Cermet programming language, or the Cermet language |
| Identifiers: CLI, package names, tool names | `cermet` (`cermet build`, `cermet check`, `cermet fmt`) |
| Source file extension | `.cerm` (`main.cerm`, `components/Button.cerm`) |
| GitHub organization | `cermet-lang` |

Do not write "Cermet Language" or "Cermet Lang" as a proper noun. The name is Cermet. The `-lang` in `cermet-lang` is a namespace marker on GitHub, saying that the organization is the official home of the Cermet programming language project. It is not part of the name.

## The extension

`.cerm` is the first four letters of the name, so the connection is obvious. Three-letter extensions were considered and rejected because the natural candidates already carry strong meanings: `.cer` is a certificate file, `.crm` means Customer Relationship Management, `.cmt` is an OCaml compiler output.

## The organization and repositories

The official GitHub organization is `cermet-lang`. The central repository is `cermet-lang/cermet`, the canonical entry point to the implementation and the main documentation. The specification is `cermet-lang/spec`. This repository, `cermet-lang/brand`, holds the visual identity. Tools get their own repositories when their release cycle needs it (`cermet-lang/lsp`, `cermet-lang/vscode-cermet`), and their names include `cermet`.

## Why this name

The name had to work as the name of a programming language, not only carry a meaning. It is short and easy to say, concise in the Latin alphabet, natural in CLI and tool names, and works as a technical name without knowing the origin. Once the origin is known, it connects in one sentence to why the language has that name. At the time of the survey in 2026-09 no strong collision was found in the developer, compiler, or runtime areas.

Other candidates in the final round were **Rutile** (a mineral that keeps its crystal structure inside other minerals; already used by several software projects), **Etale** (from étale in algebraic geometry, globally different but locally corresponding; needs mathematical background to explain and loses its accent in ASCII), and **Isuka** (the crossbill and the woodworking joint named after it; in Japanese also tied to an idiom for things that do not mesh). Cermet satisfied all the conditions at once, which none of the others did.

The trademark and name survey was a preliminary screening and is to be repeated before public release if needed.
