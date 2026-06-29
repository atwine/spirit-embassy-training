# Changelog

All notable changes to this project are documented here.  
Format: `[version / date] — commit hash — description`

---

## [2026-06-29] — `a10e202` — Modern Ministry Light + Sidebar Navigation ✅ CURRENT

### What was achieved
- Complete visual redesign of both pages to **Modern Ministry Light** theme
- `study.html` restructured from a single long scroll into a **two-column layout** with a sticky sidebar
- Logo added to both pages

### index.html changes
- New design: white background, Inter font, dark hero section with gold accent pill label
- Sticky top navigation bar with logo
- Stats strip: 2 Chapters · 15 Quiz Questions · 2 Instructors · Free
- Chapter cards section showing what's inside before registering
- Key quote strip (dark background, white text)
- Secondary registration CTA at the bottom (gold background)

### study.html changes
- **Sticky left sidebar** (260px) with full topic navigation for both chapters
- **34 anchor links** — every h3 heading wired to a sidebar link
- `scroll-margin-top: 80px` fix so sticky header no longer obscures anchor targets
- Active sidebar highlight via `IntersectionObserver` — tracks scroll position
- Body text justified with CSS `hyphens: auto`
- Labels, pull quotes, memory verse text excluded from justification
- Responsive: sidebar becomes horizontal scrollable strip under 960px

### Shared changes
- `images/logo.png` added to repository
- Logo displayed in nav (index) and sticky header (study)
- Google Fonts updated: Inter + Lora (replacing Cormorant Garamond + Lato)

---

## [2026-06-29] — `7ac2f1f` — Quiz Form Hidden Field Names Fixed

### What was achieved
- Confirmed Tally quiz hidden field names are `first_name` and `last_name`
- JS in `study.html` updated to forward parameters using exact underscore names

---

## [2026-06-29] — `6928e3a` — Quiz Autofill Slug Correction

- Updated quiz URL parameter names to use hyphenated slugs for Tally visible field autofill

---

## [2026-06-29] — `4c9f5b9` — Name Forwarding to Quiz Form

### What was achieved
- JavaScript added to `study.html` to read `first_name` and `last_name` from the URL
- Quiz button href is dynamically updated to include those parameters
- This allows the Tally quiz form to pre-fill the participant's name

---

## [2026-06-29] — `a1fb339` — Actual Tally Quiz Form Link Added

- Quiz CTA in `study.html` updated to point to `https://tally.so/r/PdgBde`

---

## [2026-06-29] — `7554767` — Actual Tally Registration Form Link Added

- Registration button in `index.html` updated to point to `https://tally.so/r/1AxJZ1`

---

## [2026-06-29] — `dfa0350` — Duplicate CTA Removed

- `index.html` had two "Register to Begin" buttons
- Bottom duplicate removed, hero button kept

---

## [2026-06-28] — `10532ed` — Two-Page Structure (Registration Gating)

### What was achieved
- Original single `index.html` split into two pages:
  - `index.html` — landing/registration page only
  - `study.html` — full study content gated behind Tally registration
- Tally form configured to redirect to `study.html` after submission
- This ensures only registered users access the study material

---

## [2026-06-28] — `29ebd6e` — README Updated

- README updated to reflect broader Spirit Embassy training scope (not just one course)

---

## [2026-06-28] — `2121a6e` — Initial Study Guide Published

### What was achieved
- First version of the study guide site live on GitHub Pages
- Single `index.html` with full content for Chapters 6 & 7
- Design: dark theme (`#0a0a0a`), Cormorant Garamond + Lato fonts, gold accents
- Scripture blocks, pull quotes, write-down panels, discussion questions
- Memory verse and 7-Day Challenge sections

---

## Next Steps / Ideas

- [ ] Add a thank-you / completion page after the quiz
- [ ] Add a second course when new material is taught
- [ ] Consider adding a PDF download of the study notes
- [ ] Analytics — track how many people complete the quiz (Tally dashboard)
- [ ] Consider a progress indicator showing % of study material read
