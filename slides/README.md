# CEF 2026 talk — *A Community Reference Library for Computational Economics*

A short (~10 minute) reveal.js presentation for QuantEcon's slot at the CEF 2026
pre-conference meeting (Venice, 28 June 2026). Modern web slides with QuantEcon
branding, built with [Quarto](https://quarto.org).

## Files

| File | What it is |
|---|---|
| [`slides.qmd`](slides.qmd) | The deck (Markdown + reveal.js). Speaker notes are in `::: {.notes}` blocks. |
| [`theme/quantecon.scss`](theme/quantecon.scss) | QuantEcon brand theme — palette + fonts. |
| [`assets/`](assets/) | Logo marks. |

## Build locally

```sh
make          # render slides.html (self-contained)
make preview  # live-reloading preview in the browser
make clean
```

`slides.html` embeds its resources (`embed-resources`), so it runs from a single
file and works offline — with one caveat: fonts load from Google Fonts when
online, falling back to a system stack offline. It is git-ignored here — it's a
build artifact.

## Publishing

On every push to `main` that touches `slides/`, the
[`Publish slides`](../.github/workflows/deploy.yml) workflow renders the deck
with Quarto and deploys it to **GitHub Pages** (served as `index.html`).

> One-time setup: in **Settings → Pages**, set *Source* to **GitHub Actions**.

## Presenting

- **Speaker notes:** press `S` for the speaker view (notes + timer + next slide).
- **Overview:** press `O` (or `Esc`) for a grid of all slides.
- **Navigate:** arrow keys / space.
