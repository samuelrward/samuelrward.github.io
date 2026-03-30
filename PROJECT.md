# PROJECT.md — CV & Publications page

## Goal
Build out `cv_publications.html` from its current stub into a complete, styled page consistent with the rest of the site.

## Page structure
Build the page in this order, as distinct sections:

### 1. Career timeline

Add an interactive HTML/CSS/JS career timeline immediately after the `<h2>CV & Publications</h2>` heading. Implement it as a self-contained `<div>` with an inline `<style>` block and inline `<script>` — do not add any external dependencies.

**Layout** (top to bottom):
- Above-labels row (height ~110px): bar-group divs containing both the label and bar for each career position, anchored to the bottom of the row
- Axis line (2px, full width)
- Year labels row: years 2020–2027 centred on their tick positions, close beneath the axis
- Below row: qualification markers with vertical connector lines

**Career positions** (above axis, coloured bars):

| Position | Start | End | Colour |
|---|---|---|---|
| PhD Student, | 2020.5 | 2023.5 | `#0072BC` |
| ESO 🇩🇪 | | | |
| PGR, | 2023.5 | 2024.5 | `#002147` |
| Newcastle University 🇬🇧 | | | |
| Flatiron Research Fellow, | 2024.5 | 2027.5 | `#C0392B` |
| CCA 🇺🇸 | | | |

Each bar has three lines of label text above it (title with comma, institute with comma, flag emoji). Label colour matches bar colour. Flag emoji should be font-size ~15px, other text ~12–13px. Hovering anywhere over a bar-group (label or bar) dims both bar and label to opacity 0.65/0.5 with a 0.18s transition.

**Qualifications** (below axis, dot markers):

| Degree | Year | University |
|---|---|---|
| *MPhys*, | 2020.5 | Durham University |
| *Dr. rer. nat.*, | 2024.5 | LMU Munich |

Each qualification: a 20px vertical line descending from the axis, then a 9px dot, then two lines of text below (degree in italics with comma, university). Default colour `var(--color-text-secondary)`. On hover, dot fills and text turns the site's standard Strata template orange — if you are unsure of the exact hex, check `assets/css/main.css` for the accent/link colour and use that; if still unclear leave a `<!-- REVIEW: confirm orange hex -->` comment.

**Axis ticks**: major ticks (8px) at each whole year, minor ticks (5px) at each half year.

**Timeline range**: 2019.7 to 2028.0.

**Sizing note**: ensure the component is appropriately sized for a full-width page section — text and flags should be clearly legible, not cramped.

### 2. CV section
- Embed the CV PDF using `<iframe>` with a sensible default height (e.g. 800px) and full width
- The PDF lives at `files/ward_cv.pdf` (relative path for local use; full URL: `https://samuelrward.github.io/files/ward_cv.pdf`) — this file does not exist yet, so use a placeholder (inline SVG or styled div) labelled `PLACEHOLDER: files/ward_cv.pdf`
- Below the embed, add a clearly labelled download button/link: `<a href="files/ward_cv.pdf" download>`
- Add a short note in small text beneath: "If the PDF does not display, use the download link above." (mobile/browser fallback caveat)

### 3. Publication libraries section

Place this section **before** the CV section (i.e. order on page is: timeline → publications → CV).
- Heading: "Publications"
- Two prominent linked buttons or styled links:
  - NASA ADS: `https://ui.adsabs.harvard.edu/search/q=orcid%3A0000-0001-5345-0900&sort=date%20desc%2C%20bibcode%20desc&p_=0`
  - ORCID: `https://orcid.org/0000-0001-5345-0900`
- Both should open in a new tab (`target="_blank"`)
- Brief line of context, e.g. "A full list of my publications is available via NASA ADS and ORCID."

## Style requirements
- Match the header, nav, and footer structure of `index.html` exactly
- Use existing Strata template CSS classes throughout — do not add custom CSS
- Accessible but professional tone (see CLAUDE.md)

### 3. Contact block
- Add the contact block from `index.html` to the bottom of every stub page: `cv_publications.html`, `research.html`, `outreach.html`, `interests.html`
- Copy it exactly as-is, including the website URL line — keep all 4 lines for visual balance even though the URL is technically redundant on internal pages

## Files to create / modify
| File | Action |
|------|--------|
| `cv_publications.html` | Replace stub content with sections above; add contact block |
| `research.html` | Add contact block only |
| `outreach.html` | Add contact block only |
| `interests.html` | Add contact block only |
| `files/ward_cv.pdf` | Do not create — add placeholder reference only |

## Do not touch
- `index.html`
- `assets/`
- `images/`

## Definition of done
- Page renders correctly when opened locally in a browser
- Placeholder is clearly labelled and visually obvious
- Header/nav/footer matches the rest of the site
- Changes staged and committed with message: `Build out CV & Publications page`
- Do not push