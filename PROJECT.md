# PROJECT.md — Research page

## Goal
Build out `research.html` from its current stub into a complete, styled page consistent with the rest of the site.

## General rules
- Match header, nav, footer and contact block structure of `index.html` exactly
- Use existing Strata template CSS classes throughout — do not add custom CSS unless strictly necessary
- All images: `object-fit: contain` — preserve aspect ratio, no cropping
- Accessible but professional tone (see CLAUDE.md)
- Inline `<!-- REVIEW: ... -->` comments for anything uncertain

---

## Page structure

### Intro section
Heading (already present as stub `<h2>`): **How do outflows from Active Galactic Nuclei impact the evolution of galaxies?**

Intro paragraph:

> Most massive galaxies harbour a supermassive black hole at their centre. For much of their lives these black holes lie dormant, but if fed with enough gas, they can form active galactic nuclei (AGN), releasing a huge amount of energy. This energy can drive powerful outflows back into the galaxy, both in the form of winds and jets. My research asks how these outflows interact with the surrounding gas, and whether they can suppress star formation and quench the galaxy's growth.

---

### Block 1 — Wind-ISM simulations

**Section heading:** Wind-ISM simulations

**Layout:** Two-column row — images stacked on the left, all three paragraphs as a single text column on the right. Images and text are not 1-to-1 paired; the text flows as one continuous block beside both images.

- Left column: two images stacked vertically with a small gap
  - `PLACEHOLDER: images/research_acdc_1.jpg`
  - `PLACEHOLDER: images/research_acdc_2.jpg`
- Right column: three paragraphs in sequence (no sub-headings)

**Text:**

Paragraph 1:
> Understanding how AGN-driven winds couple to the ISM in galaxies is key to revealing the impact of outflows on galaxy evolution. However, resolving the small-scale interactions between AGN winds and the interstellar medium (ISM) remains computationally challenging. To study these processes directly, I created the ACDC (AGN in Clumpy DisCs) simulation suite, which combines a manually controlled clumpy ISM structure with an AGN wind model based on Costa et al. (2020), using the AREPO code (Springel et al. 2010). These simulations revealed how AGN winds launch multiphase outflows whose properties differ significantly from analytic models and simulations with underresolved ISM structure (Ward et al. 2024).

Paragraph 2:
> A longstanding problem in the field is how cold clouds survive being accelerated by an AGN wind without being destroyed. Using the ACDC simulations, we find that clouds can survive on timescales exceeding 5 Myr through efficient mixing and radiative cooling at the wind-cloud interface. In Ward et al. (2026), we investigated the X-ray emission produced by this mixing layer, showing it to be a potentially important contributor to the soft, extended X-ray excess observed in nearby quasars.

Paragraph 3:
> This work has since been extended in two directions: Ivan Almeida (MPIA, Heidelberg) developed an enhanced refinement scheme for the cold outflowing clouds, showing that higher-luminosity AGN drive denser cold outflowing clouds with important implications for how outflow properties are inferred observationally (Almeida et al. 2026). PhD student Houda Haidar (Newcastle University) is incorporating a dust sputtering destruction model to study dusty outflows (Haidar et al., in prep.).

---

### Block 2 — Mock radio observations

**Section heading:** Mock radio observations

**Layout:** Three-row stack, image side alternates right (i.e. this block is right-image to alternate with Block 1's left-image):

- Row 1: main summary figure, centred, max-width ~70% of content area, `object-fit: contain`
  - `PLACEHOLDER: images/research_sangria_summary.jpg` — horizontal aspect ratio ~1.5-2:1
- Row 2: two columns — text paragraph left, SANGRiA logo right (logo smaller, ~25% width, `object-fit: contain`)
  - `PLACEHOLDER: images/research_sangria_logo.jpg`

**Text:**

> Radio observations offer a unique window into AGN feedback - from high-energy non-thermal emission to 21cm spectra of neutral hydrogen. Working with CCA predoctoral researcher Emily Kerrison (University of Sydney), I developed SANGRiA (Simulating Absorption of Neutral Gas for Radio Astronomy), a forward-modelling pipeline for 21cm HI absorption. SANGRiA takes galaxies from the SIMBA cosmological simulation, adds jet models, and uses these as backlights for HI absorption radiative transfer. In Kerrison et al. (2026, submitted to ApJ), we apply this to the ASKAP-FLASH survey to investigate the overrepresentation of compact radio sources in their HI-detected sample. A forthcoming companion paper (Ward, Kerrison & Tonnesen) will present the full SANGRiA framework and demonstrate its applicability across current and future radio telescopes including MeerKAT, the SKA, and the DSA.

---

### Block 3 — Cosmological simulations

**Section heading:** Cosmological simulations

**Layout:** Two-column — figure left, text right. Figure is vertical aspect ratio so standard side-by-side works well.

- Left: `PLACEHOLDER: images/research_cosmo.jpg` — vertical aspect ratio
- Right: one paragraph

**Text:**

> Cosmological simulations such as IllustrisTNG, EAGLE, and SIMBA require AGN feedback to reproduce observed galaxy properties, including stellar mass functions. However, observational studies consistently find AGN preferentially in gas-rich, star-forming galaxies, leading some to question whether AGN feedback is truly effective. In Ward et al. (2022), we analysed these simulations using the same techniques applied to observational samples, finding that simulations also predict AGN to inhabit gas-rich, star-forming hosts despite employing effective feedback models. This demonstrates that the absence of population-level evidence for feedback cannot be used to rule out AGN-driven quenching. This simulation analysis was subsequently incorporated into observational studies of AGN host galaxies by Bertola et al. (2024) and Frias Castillo et al. (2024).

---

## Files to create / modify
| File | Action |
|------|--------|
| `research.html` | Replace stub content with sections above |
| `images/` | Do not add — use clearly labelled SVG placeholders per CLAUDE.md |

## Do not touch
- `index.html`
- `cv_publications.html`
- `assets/`

## Citation links
Every paper cited in the text must be wrapped in an `<a href="..." target="_blank">` tag linking to its NASA ADS entry. Papers to link:
- Ward et al. 2022
- Ward et al. 2024
- Ward et al. 2026
- Costa et al. 2020
- Springel et al. 2010
- Almeida et al. 2026
- Kerrison et al. 2026
- Bertola et al. 2024
- Frias Castillo et al. 2024

Use the site's standard orange accent colour for all citation links — check `assets/css/main.css` for the hex value and apply it inline or via a class. If an ADS entry cannot be found for a paper, leave a `<!-- REVIEW: ADS link needed for X -->` comment in place.

## Definition of done
- Page renders correctly when opened locally in a browser
- All placeholders clearly labelled and visually obvious
- Header/nav/footer/contact block matches the rest of the site
- Changes staged and committed with message: `Build out Research page`
- Do not push