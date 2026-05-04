# The Magic Map — Module 4 (Spatial Statistics)

A Quarto **revealjs** slide deck adapting the *Magic Map* PDF into a clean,
stat4research.com-flavoured presentation. Inspired by Andy Teucher's
[Advanced R Package Development deck](https://andyteucher.ca/dfo-advanced-r-pkgs-2026/slides/package-fundamentals-slides.html).

## Files

| File | Purpose |
|---|---|
| `the-magic-map.qmd` | the slides (source) |
| `custom.scss`       | the theme — deep navy / warm sand / soft gold |

## Render

From R / RStudio:

```r
quarto::quarto_render("the-magic-map.qmd")
```

From the terminal:

```bash
quarto render the-magic-map.qmd
```

This produces `the-magic-map.html` — open it in a browser. Press `?` for
keyboard shortcuts, `S` to open speaker notes, `F` for fullscreen.

## Structure

The deck follows the PDF's narrative arc, organised into 5 sections:

1. **The Challenge** — discrete points vs. fluid ocean, Tobler's First Law
2. **The Gaussian Random Field** — invisible sheet + Matérn covariance
3. **The Computational Trick** — Big-N problem, SPDE mesh, mesh design
4. **Putting It Together** — model integration + `sdmTMB` example
5. **What's Next** — pointer to spatio-temporal models (Module 5)

## Customisation tips

- Swap the navy section background by editing the `{background-color="..."}`
  attributes after each `#` heading.
- The colour palette lives at the top of `custom.scss` — change five
  variables and the whole deck re-themes.
- For French audiences: the technical terms (GRF, SPDE, Matérn) stay in
  English by convention, but the surrounding prose translates cleanly.

## Dependencies

- Quarto ≥ 1.4
- A recent browser (for MathJax + reveal.js)
- *Optional for the live R demo*: `sdmTMB`, `INLA`, `fmesher`
