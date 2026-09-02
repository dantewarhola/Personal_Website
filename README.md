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
