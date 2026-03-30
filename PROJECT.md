# PROJECT.md — CV & Publications page

## Goal
Build out `cv_publications.html` from its current stub into a complete, styled page consistent with the rest of the site.

## Page structure
Build the page in this order, as distinct sections:

### 1. CV section
- Embed the CV PDF using `<iframe>` with a sensible default height (e.g. 800px) and full width
- The PDF lives at `files/ward_cv.pdf` (relative path for local use; full URL: `https://samuelrward.github.io/files/ward_cv.pdf`) — this file does not exist yet, so use a placeholder (inline SVG or styled div) labelled `PLACEHOLDER: files/ward_cv.pdf`
- Below the embed, add a clearly labelled download button/link: `<a href="files/ward_cv.pdf" download>`
- Add a short note in small text beneath: "If the PDF does not display, use the download link above." (mobile/browser fallback caveat)

### 2. Publication libraries section
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