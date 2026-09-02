# Dante Warhola — Cybersecurity Portfolio

A multi-page personal résumé and portfolio site focused on cybersecurity and cyber engineering.
Plain static HTML, one shared stylesheet, one small JavaScript file. **No build step, no framework,
no dependencies.**

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home — hero, focus areas, featured projects |
| `about.html` | Bio, education, skills matrix, certifications, leadership |
| `experience.html` | Work history timeline + recommendation |
| `projects.html` | Security-focused projects and home labs |
| `building-with-claude.html` | Security tooling built with Claude Code |
| `resume.html` | Web résumé + PDF download + verified credentials |
| `contact.html` | Email, LinkedIn, GitHub, location |
| `404.html` | Custom not-found page |

## Structure

```
Personal_Website/
├── *.html                     the pages above
├── vercel.json                clean URLs + asset caching
├── assets/
│   ├── css/style.css          full design system (dark theme)
│   ├── js/main.js             mobile nav, active link, scroll reveal
│   ├── img/                   headshot, favicon, social image
│   └── docs/                  résumé, Security+ certificate, recommendation letter (PDF)
└── README.md
```

## Preview locally

Just open `index.html` in a browser. Or serve the folder for clean URLs:

```bash
# Python
python -m http.server 8000
# or Node
npx serve .
```

Then visit <http://localhost:8000>.

## Deploy

### 1. Push to GitHub

```bash
cd Personal_Website
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/dantewarhola/<repo-name>.git
git push -u origin main
```

### 2. Import to Vercel

1. Go to <https://vercel.com/new> and import the repo.
2. **Framework Preset:** `Other`.
3. **Build Command:** leave empty. **Output Directory:** leave empty (repo root is served as-is).
4. Deploy. Every push to `main` redeploys automatically.

`vercel.json` enables clean URLs (`/about` instead of `/about.html`) and long-lived caching for
everything under `/assets`. Internal links keep the `.html` suffix so the site also works when opened
directly from disk.

## Editing content

- **Text and links:** edit the relevant `.html` file directly. The header and footer markup is
  duplicated in every page — update all of them together if you change navigation.
- **Colors, spacing, typography:** `assets/css/style.css`, top of the file (`:root` custom
  properties).
- **Résumé / certificate / letter:** replace the PDFs in `assets/docs/` (keep the same filenames).
- **Headshot:** replace `assets/img/headshot.jpg` (square image, ~600×600 or larger).

## Source material

These files in this folder are the originals the site content was drawn from. They are **not used by
the site** and can be deleted once you're happy with it:

- `135896896.jpg` — original headshot (a copy is at `assets/img/headshot.jpg`)
- `Dante_Warhola_resume_8_28_26.pdf`, `sec_cert.pdf`, `TBS_Letter_Of_Recommendation.pdf` — originals
  (renamed copies are in `assets/docs/`)
- `Screenshot 2026-09-02 *.png` — LinkedIn screenshots used for reference

## Notes

- `assets/img/og-cover.svg` is the social-share image. Some link scrapers don't render SVG — if
  Twitter/LinkedIn previews matter, export it to a 1200×630 PNG and update the `og:image` tags.
- No analytics or trackers are included.
