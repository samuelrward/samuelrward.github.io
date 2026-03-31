# PROJECT.md — Responsive stress test

## Goal
Check all pages render correctly across common screen widths and fix any layout issues found. Make the image credit text stick to the bottom of the sidebar on all pages.

## General rules
- Do not edit `assets/css/main.css` — use inline `<style>` blocks or inline styles to apply fixes
- Do not edit images
- Commit all fixes in a single commit with message: `Responsive fixes and sidebar credit pin`
- Do not push

---

## Task 1 — Pin sidebar image credit to bottom

On all pages, the image credit text in the sidebar should be pinned to the bottom of the sidebar regardless of content length. Apply a minimal inline `<style>` block override to each page to achieve this without touching `assets/css/main.css`.

---

## Task 2 — Responsive layout fixes

Test each page at the following widths and fix any issues found:
- Mobile: 375px
- Tablet: 768px  
- Desktop: 1280px+

### Known issue to fix
**CV & Publications page:** The thesis download button can extend beyond the right edge on mobile. If it overflows, move it to its own row below the other buttons.

### Things to check on every page
- Nav links — no overlap or overflow
- Two-column image + text layouts — should stack vertically on mobile (image above text)
- Text — no horizontal overflow or clipping
- No unintended horizontal scrolling at any width

### Page-specific things to check
- **CV & Publications:** Timeline — this is the most complex element. On mobile, if the timeline becomes unreadably small, add a short note beneath it (e.g. "Best viewed on desktop") rather than attempting a full mobile reflow of the timeline
- **CV & Publications:** PDF iframe — should scale to full width on mobile
- **Research:** Two-column image + text blocks — stack on mobile
- **Research:** SANGRiA summary figure (centred, 70% width) — should scale down gracefully
- **Outreach & Community:** Two-column blocks — stack on mobile
- **Personal Interests:** Book carousel — 4 columns is too many for mobile; reduce to 2 columns on screens below 600px
- **Personal Interests:** Lightbox overlay — should work correctly on mobile tap

### Fix approach
- Use CSS media queries in an inline `<style>` block on each page where fixes are needed
- Prefer `flex-direction: column` for stacking two-column layouts on mobile
- Keep fixes minimal — do not restructure pages, only adjust layout behaviour

---

## Files to modify
All `.html` files in the repo root as needed. Do not modify `assets/`.

## Definition of done
- All pages checked at 375px, 768px, and 1280px
- Known thesis button overflow fixed
- Sidebar credit pinned to bottom on all pages
- No horizontal scrolling on any page at any tested width
- Timeline has a "best viewed on desktop" note if unreadable at 375px
- Book carousel shows 2 columns on mobile
- Changes staged and committed
- Do not push