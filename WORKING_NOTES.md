# Working Notes — 3300 Landing Page

> **Internal document — not intended for public audiences.**
> This file is for developer and AI assistant reference only. Update it at the end of every working session before closing the project.

---

## 1. How to Use This File (For AI Assistants)

1. Read this entire file before suggesting changes or writing any code.
2. Read `README.md` for the public-facing project description and feature list.
3. Read `PRD.md` for content requirements and target audience definition.
4. Read `STANDARDS.md` for technical and design rules — every rule there applies without exception.
5. Do not change the folder structure or file naming conventions without discussing it first.
6. Follow all conventions listed in Section 8 exactly.
7. Do not suggest any approach listed in "What Was Tried and Rejected" (Section 10).
8. Ask a clarifying question before making any large structural change (adding JavaScript, changing layout system, splitting into multiple pages, etc.).
9. This project was built with AI assistance (Replit Agent). Refactor conservatively — prefer targeted edits over rewrites.

---

## 2. Current State

**Last Updated:** 2026-03-23

This is a complete, working static personal landing page. All required content sections from the PRD are built and styled. The site is live in the Replit environment and served via Python's built-in HTTP server on port 5000. No known rendering errors.

### What Is Working

- [x] Sticky navigation bar with smooth-scroll anchor links
- [x] Hero section — circular headshot, name, tagline, LinkedIn and GitHub buttons
- [x] About Me section — bio, Dean's List mention, target market
- [x] Skills section — three labeled groups (Tools, Visualization, Techniques) displayed as pill badges
- [x] Projects section — three cards in a two-column desktop grid (MLB regression, MLB SQL database, Car Value scraping)
- [x] Experience section — three roles with organization, location, dates, and bullet achievements
- [x] Contact section — card links for LinkedIn, email, and GitHub
- [x] Footer with copyright
- [x] Fully responsive from 320px (single column mobile, two-column project grid on desktop)
- [x] Inter font loaded from Google Fonts
- [x] All external links use `rel="noopener noreferrer"` and open in a new tab
- [x] `README.md` written and committed
- [x] Deployment configured as a static site

### What Is Partially Built

- [ ] Car Value Analysis project card — description is accurate but brief; no bullet-level detail exists because the resume did not include it (need: actual project details from the student)

### What Is Not Started

- [ ] `js/scripts.js` — directory exists but file is empty; no JavaScript is used currently
- [ ] Favicon — no icon file added yet
- [ ] LICENSE file — needs to be created on GitHub (MIT)

---

## 3. Current Task

**What I was working on when I last stopped:** The initial build is complete. All HTML and CSS files were written, the README and WORKING_NOTES were generated, and the site was verified working in the Replit preview. The deployment was configured as a static site.

**The very next step is:** Add a favicon (`images/favicon.ico` or `.png`) and reference it in the `<head>` of `index.html`.

---

## 4. Architecture and Tech Stack

| Technology | Version | Why It Was Chosen |
|---|---|---|
| HTML5 | Current | Required by STANDARDS.md; semantic elements improve accessibility and SEO |
| CSS3 | Current | Required by STANDARDS.md; vanilla CSS keeps the project dependency-free and easy to maintain |
| Inter (Google Fonts) | Variable | Specified in STANDARDS.md as both the heading and body font; clean, professional, highly legible |
| Python `http.server` | 3.x (system) | Zero-dependency local dev server; no npm or Node required for a static site |
| No JavaScript framework | — | STANDARDS.md explicitly requires a static site with no JavaScript; kept intentionally |

---

## 5. Project Structure Notes

```
3300-landing-page/
├── index.html                        # Single-page HTML — all content; do not split into multiple pages
├── css/
│   └── stylesheet.css                # All styles; no inline CSS anywhere — enforced by STANDARDS.md
├── js/                               # Reserved for future scripts; currently empty
├── Images/
│   └── Image1.jpg                    # Professional headshot; referenced as Images/Image1.jpg (capital I)
├── PRD.md                            # Content requirements — source of truth for what must appear
├── STANDARDS.md                      # Technical and design rules — read before every session
├── README.md                         # Public-facing documentation
├── WORKING_NOTES.md                  # This file
├── Christopher Willcutt Resume.pdf   # Content reference only — not linked from the site
└── Test                              # Legacy file from original repo clone — can be removed
```

**Non-obvious decisions:**

- The `Images/` folder uses a capital `I` because that is how it was committed in the original repository. All references in `index.html` use `Images/Image1.jpg` (capital I) to match. Do not rename this folder without updating the reference.
- `js/` exists because STANDARDS.md defines it in the folder structure, but no JS is used. Do not add scripts without confirming with the student first.
- `Christopher Willcutt Resume.pdf` is in the root for reference during development. STANDARDS.md explicitly says do not link to or embed the resume from the site.
- `Test` is an artifact from the original repo clone (duplicate of the original index.html). It serves no purpose and can be deleted.

**Files that must not be changed without discussion:**
- `STANDARDS.md` — defines all rules; edits here affect the entire project
- `PRD.md` — defines required content; do not remove required sections
- `Images/Image1.jpg` — the student's professional headshot

---

## 6. Data / Database

This project has no persistent data, database, or flat data files. All content is hardcoded directly in `index.html`. There is no server-side logic, no API, and no user-submitted data.

---

## 7. Conventions

### File and Folder Naming
- HTML file: `index.html` (lowercase)
- Stylesheet: `css/stylesheet.css` (lowercase)
- Images folder: `Images/` (capital I — match existing)
- Do not create additional HTML files; this is a single-page site

### Code Style
- No inline styles anywhere — all styling goes in `css/stylesheet.css`
- No `<style>` tags in `index.html`
- Semantic HTML5 elements used throughout: `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<nav>`
- All images have descriptive `alt` attributes
- External links always include `target="_blank" rel="noopener noreferrer"`
- Heading hierarchy is strict: one `<h1>` per page, `<h2>` for section titles, `<h3>` for subsections
- Proper heading hierarchy: h1 → h2 → h3 (no skipping levels)

### CSS Conventions
- CSS is organized top-to-bottom matching document order: Reset → Typography → Nav → Hero → About → Skills → Projects → Experience → Contact → Footer → Responsive
- Section comments delimit each block using `/* === Section Name === */`
- Colors use the exact hex values from STANDARDS.md: `#F8F9FA`, `#212529`, `#0D6E6E`, `#E9ECEF`
- Max content width: 800px, centered with `margin: auto`
- No CSS frameworks, no utility classes, no external CSS files besides `stylesheet.css`

### Git Commit Style
- Imperative present tense: "Add contact section styles" not "Added" or "Adding"
- Keep messages concise and descriptive of what changed

---

## 8. Decisions and Tradeoffs

- **No JavaScript:** STANDARDS.md requires a fully static site. Even simple interactions like a hamburger menu or animations were excluded to stay compliant. Do not suggest adding JS unless the student explicitly changes this requirement.
- **Single HTML file:** All content lives in `index.html`. STANDARDS.md scopes this to a single page. Do not suggest splitting into multiple HTML files.
- **Python dev server instead of Node/npm:** The project has no build step and no dependencies, so Python's built-in server is the simplest option that requires nothing extra installed. Do not suggest switching to a Node-based dev server unless the project adds JavaScript.
- **Google Fonts CDN for Inter:** Inter was specified in STANDARDS.md. Loading via CDN avoids storing font files locally and keeps the repo clean. A downside is it requires internet access to render correctly; this is accepted.
- **Images folder capitalized:** The original repo committed the folder as `Images/`. Keeping the capital avoids breaking the existing reference and any git history confusion.
- **Inline hero layout via CSS flexbox:** The hero uses flexbox to place the photo beside the text on desktop and stacks them on mobile. CSS Grid was not needed for a two-element layout.
- **Two-column project grid at 640px breakpoint:** STANDARDS.md specifies two-column desktop for projects. 640px was chosen as the breakpoint because it cleanly accommodates two ~360px cards with a 24px gap inside an 800px container.

---

## 9. What Was Tried and Rejected

- **Placeholder/lorem ipsum text:** The student's PRD explicitly prohibited it. Every piece of text is drawn from the resume, PRD, or LinkedIn information. Do not suggest adding placeholder content.
- **CSS framework (Bootstrap, Tailwind):** STANDARDS.md prohibits frameworks — vanilla CSS only. Do not suggest these.
- **Multi-page layout:** STANDARDS.md and PRD both define this as a single-page site. Do not suggest breaking it into separate pages.
- **Embedding the resume PDF:** STANDARDS.md explicitly says not to link to or embed the resume. Do not suggest this.

---

## 10. Known Issues and Workarounds

- **Car Value Analysis project has a thin description:** The resume contained no bullet points for this project, so the card was written using only the PRD description ("Python web scraping to analyze car values"). No workaround needed — the student should supply additional details when available and the card can be updated.
- **`Test` file in root:** An artifact from the initial repo clone. It is a copy of the original "Hello World" HTML and serves no purpose. No workaround — it can simply be deleted.
- **No favicon:** The browser tab shows a generic icon. No workaround in place. Fix: create a favicon and add `<link rel="icon" href="images/favicon.png">` to the `<head>`.

---

## 11. Browser / Environment Compatibility

**Expected to work (per STANDARDS.md):** Chrome, Safari, Firefox, Edge, and mobile browsers (iOS Safari, Android Chrome).

**Tested:** Chrome (Replit preview), verified rendering via screenshot at time of build.

**Known incompatibilities:** None identified. The site uses no experimental CSS features — flexbox, grid, and custom properties are all baseline-supported across modern browsers.

**Environment:** Replit (NixOS), Python 3.x system install, no Node or npm required.

---

## 12. Open Questions

- Should the Car Value Analysis project card be expanded once the student documents that project? If so, what details should be added?
- Should the experience section be kept, or does the student prefer to keep the page focused on analytics skills and projects only?
- Does the student want a downloadable resume link in the future? (Currently excluded per STANDARDS.md.)
- Should a favicon be added, and if so, should it be a custom graphic or a simple initial-based icon?
- Is the `Test` file in the root safe to delete, or was it intentional?

---

## 13. Session Log

### 2026-03-23
- Set up Replit environment: configured Python HTTP server workflow on port 5000, verified site loads
- Read PRD.md, STANDARDS.md, and extracted content from `Christopher Willcutt Resume.pdf`
- Built complete `index.html` with all required sections: hero, about, skills, projects, experience, contact, footer
- Built complete `css/stylesheet.css` with all design standards applied
- Verified site renders correctly in Replit preview via screenshot
- Configured static site deployment
- Generated `README.md` with all required sections (badges, features, tech stack, changelog, etc.)
- Generated `WORKING_NOTES.md` (this file)
- Left incomplete: favicon, `js/scripts.js`, LICENSE file on GitHub, Car Value project detail
- Next step when resuming: add a favicon and delete the `Test` file

---

## 14. Useful References

- [STANDARDS.md](STANDARDS.md) — Primary rule document for this project; read first every session
- [PRD.md](PRD.md) — Content requirements and target audience definition
- [MDN HTML5 Semantic Elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantics_in_html) — Reference for correct semantic element use
- [MDN CSS Flexbox Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox) — Used for hero layout and nav layout
- [MDN CSS Grid Guide](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout) — Used for the two-column project card grid
- [Google Fonts — Inter](https://fonts.google.com/specimen/Inter) — Font used throughout
- [shields.io](https://shields.io/) — Badge generation for README
- [WCAG 2.2 Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/) — Accessibility standard this project targets (Level AA)
- **AI tools used:** Replit Agent was used to generate the initial `index.html`, `css/stylesheet.css`, `README.md`, and this `WORKING_NOTES.md`. All output was reviewed by the author. Any future AI sessions should read this file first before making suggestions.
