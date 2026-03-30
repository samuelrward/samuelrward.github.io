# PROJECT.md — Outreach & Community page

## Goal
Build out `outreach.html` from its current stub into a complete, styled page consistent with the rest of the site.

## General rules
- Match header, nav, footer and contact block structure of `index.html` exactly
- Use existing Strata template CSS classes throughout — do not add custom CSS unless strictly necessary
- All links use the site's standard orange accent colour — check `assets/css/main.css` for the hex value
- All external links open in a new tab (`target="_blank"`)
- Accessible but professional tone (see CLAUDE.md)
- Inline `<!-- REVIEW: ... -->` comments for anything uncertain

---

## Page structure

### Block 1 — Public engagement

**Section heading:** Public engagement

**Layout:** Two columns — image left (~38% width), text right. Image may be cropped/zoomed to fit. Caption below image.

- Left: `PLACEHOLDER: images/outreach_talks.jpg` with caption `<!-- REVIEW: add caption text -->`
- Right: text block (three paragraphs, see below)

**Text:**

Paragraph 1:
> A huge advantage we have as astronomers is that so many people - of all ages and from all walks of life - are interested in the universe and the work we do studying it. I enjoy sharing my work through public outreach talks, including at Pint of Science Munich (2023), Newcastle University's <a href="https://www.youtube.com/watch?v=4DADgIvBPHo&list=PLMaRMFMkiHN6Oleg8ls2EN8DdV5fzdnuG&index=4">INSIGHTS public lecture series</a> (2023), and the Royal Observatory Greenwich <a href="https://www.youtube.com/watch?v=9_VtBM9xtmY">Think Space online lecture series</a> (2025), where my talk <em>An Extragalactic Murder Mystery: Do Black Holes Kill Galaxies?</em> is available to watch.

Paragraph 2:
> I was part of the team behind <a href="https://www.spaceinvestigators.com/">Space Investigators North East</a>, a special exhibit at the Great North Museum: Hancock in Newcastle. I directed and edited a <a href="https://www.spaceinvestigators.com/astronomer-interviews">film</a> of interviews with researchers from Newcastle, Northumbria, and Durham - situated within a life-size model of the JWST mirror - celebrating the breadth of astrophysical research in the North East and the diverse backgrounds of the scientists behind it.

Paragraph 3:
> As part of the Simons Foundation's Open Interval program, which fosters collaborations between scientists and artists, I have been paired with choreographer <a href="https://www.jieminyang.art/">Jiemin Yang</a> to explore the intersections between contemporary dance and my research into AGN feedback. This ongoing collaboration is developing new ways to communicate complex astrophysical ideas through movement.

---

### Block 2 — Teaching & mentoring

**Section heading:** Teaching & mentoring

**Layout:** Two columns — text left, image right (~38% width). Image may be cropped/zoomed to fit. Caption below image.

- Right: `PLACEHOLDER: images/outreach_teaching.jpg` with caption `<!-- REVIEW: add caption text -->`
- Left: text block (three paragraphs, see below)

**Text:**

Paragraph 1:
> I was lead supervisor for Emily Kerrison (University of Sydney) during her time on the CCA <a href="https://www.simonsfoundation.org/flatiron-institute-center-for-computational-astrophysics-pre-doctoral-program/">predoctoral program</a>, where we designed and built the SANGRiA pipeline to connect her existing expertise in ASKAP-FLASH observations with cosmological simulations. Mentoring Emily through her first simulation-based project was one of the highlights of my fellowship so far.

Paragraph 2:
> I have given guest lectures at Borough of Manhattan Community College (BMCC) for their introductory astronomy course, and an online lecture at Meru University of Science and Technology, Kenya.

Paragraph 3:
> I supervised a middle school student on a work experience placement, designing a week-long program that went from calculating foam dart trajectories to programming a simple Solar System model in Python. You can find the notebooks on <a href="https://github.com/samuelrward/SolarSystem">GitHub</a>.

---

### Block 3 — Community & service

**Section heading:** Community & service

**Layout:** Text full width, then workshop image centred below at 70% page width, `object-fit: contain` (no cropping), caption below image.

- Image: `PLACEHOLDER: images/outreach_workshop.jpg` with caption `<!-- REVIEW: add caption text -->`

**Text:**

Paragraph 1:
> As part of the CCA's Baryon Cycle strategic focus, I chaired the Scientific Organising Committee for the <a href="https://www.simonsfoundation.org/event/agn-energy-flows-workshop/">AGN & Energy Flows workshop</a> (February 2026). This brought together over 50 observers and theorists across a range of spatial scales to build a more unified picture of how energy from AGN impacts galaxies and their surroundings.

Paragraph 2:
> During my PhD at ESO I chaired the Student Representative Committee, advocating for student welfare during the cost-of-living crisis, organising mental health awareness events, and communicating student concerns to the Office for Science.

---

## Files to create / modify
| File | Action |
|------|--------|
| `outreach.html` | Replace stub content with sections above |
| `images/` | Do not add — use clearly labelled SVG placeholders per CLAUDE.md |

## Do not touch
- `index.html`
- `cv_publications.html`
- `research.html`
- `assets/`

## Definition of done
- Page renders correctly when opened locally in a browser
- All placeholders clearly labelled with correct filenames and obvious visually
- All links open in a new tab and use the site's orange accent colour
- Header/nav/footer/contact block matches the rest of the site
- Changes staged and committed with message: `Build out Outreach & Community page`
- Do not push