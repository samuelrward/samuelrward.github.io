# PROJECT.md — Personal Interests page

## Goal
Build out `interests.html` from its current stub into a complete, styled page consistent with the rest of the site.

## General rules
- Match header, nav, footer and contact block structure of `index.html` exactly
- Use existing Strata template CSS classes throughout — do not add custom CSS unless strictly necessary
- All external links open in a new tab (`target="_blank"`)
- All links use the site's standard orange accent colour — check `assets/css/main.css` for the hex value
- Accessible but professional tone (see CLAUDE.md)
- Inline `<!-- REVIEW: ... -->` comments for anything uncertain

---

## Page structure

Sections alternate image left/right with dividers between them. Order: Volleyball, Choir, Hiking, Reading.

---

### Block 1 — Volleyball

**Section heading:** Volleyball

**Layout:** Two columns — image left (~38% width), text right. Image may be cropped to fit. Caption below image.

- Left: `PLACEHOLDER: images/interests_volleyball.jpg` with caption `<!-- REVIEW: add caption text -->`

**Text:**

> I enjoy playing a range of team sports - including rugby and rowing earlier in life - and now mostly focus on volleyball. While at ESO, I helped organise the institute volleyball team, coaching weekly training sessions and captaining the side in tournaments against other research institutes at the Atomiade Summer Games in [Grenoble (2022)](https://www.asceri.eu/events/88-summer-atomiade-2022) and [Berlin (2023)](https://www.asceri.eu/events/86-mini-atomiade-2023). These days I spend my Tuesday evenings playing in a co-ed recreational league in New York City - we recently won a Santa-themed tournament.

---

### Block 2 — Choral singing

**Section heading:** Choral singing

**Layout:** Two columns — text left, image right (~38% width). Image may be cropped to fit. Caption below image.

- Right: `PLACEHOLDER: images/interests_choir.jpg` with caption `<!-- REVIEW: add caption text -->`

**Text:**

> Having sung as a choral scholar at St John's College Chapel Choir, Durham, music has remained a constant alongside my research. During my PhD I co-founded and co-directed a choir at ESO, bringing together members of all singing abilities. Our inaugural concert featured music as varied as music from Lord of the Rings, a Purcell opera movement, and a traditional South African folk song. Since moving to New York, I sing bass with the [Greenwich Village Chamber Singers](https://gvcsnyc.org/), with whom I recently performed in a sold-out concert of Bach's St Matthew Passion.

---

### Block 3 — Hiking

**Section heading:** Hiking

**Layout:** Two columns — image left (~38% width), text right. Image may be cropped to fit. Caption below image.

- Left: `PLACEHOLDER: images/interests_hiking.jpg` with caption `<!-- REVIEW: add caption text -->`

**Text:**

> After a long week of science, there's nothing better than a fresh lungful of air in the mountains. When I lived in Munich, I frequently organised "beginner-achievable" hiking trips for the other students (enjoyable even when they tipped into [Type II fun](https://weareexplorers.co/type-2-fun-guide-fun-scale/)!) Now I'm in New York, I can hop on a train up the Hudson Valley to hike in the Catskills or visit cute upstate towns (where I tried Root Beer for the first time!).

---

### Block 4 — Reading

**Section heading:** Reading

**Layout:** Text full width, then book carousel below at ~90% page width, centred.

**Text:**

> I enjoy reading, and have spent the last few years participating in a reading challenge with friends, aiming to read 15 books a year across a wide range of genres and authors. My favourites tend to cluster around science fiction, historical fiction, and non-fiction history and politics, although I've enjoyed exploring new genres I hadn't read before. I'm always open to new book recommendations!

**Carousel spec:**
- Display 8 book covers at a time in a 2-row grid of 4 columns, advancing 8 books at a time
- Book images live in `images/books/` named `book_1.jpg`, `book_2.jpg` etc. — display in ascending numerical order
- Use 8 placeholder slots if the actual images are not yet present: `PLACEHOLDER: images/books/book_1.jpg` through `PLACEHOLDER: images/books/book_8.jpg`
- All covers cropped to a consistent vertical 4:3 aspect ratio (`object-fit: cover`) so they align uniformly — most source images are already 4:3 but crop as needed
- Book title as a caption beneath each cover, `<!-- REVIEW: add book title -->`
- Left and right arrow buttons on the edges to advance/retreat one book at a time
- Arrows should wrap around (last book cycles back to first)
- No autoplay — user-controlled only
- On hover: book cover scales up slightly (e.g. `transform: scale(1.05)`) with a smooth transition, consistent with the zoom effect used on image links on the homepage
- On click: book cover opens in a lightbox-style overlay — a darkened background with the image displayed larger and centred. Clicking anywhere outside the image or on a close button dismisses the overlay
- Carousel and lightbox implemented in vanilla JS, no external libraries

---

## Files to create / modify
| File | Action |
|------|--------|
| `interests.html` | Replace stub content with sections above |
| `images/` | Do not add — use clearly labelled SVG placeholders per CLAUDE.md |

## Do not touch
- `index.html`
- `cv_publications.html`
- `research.html`
- `outreach.html`
- `assets/`

## Definition of done
- Page renders correctly when opened locally in a browser
- Carousel navigates correctly with arrow buttons, wraps around, no autoplay
- All placeholders clearly labelled with correct filenames
- All links open in a new tab and use the site's orange accent colour
- Header/nav/footer/contact block matches the rest of the site
- Changes staged and committed with message: `Build out Personal Interests page`
- Do not push 