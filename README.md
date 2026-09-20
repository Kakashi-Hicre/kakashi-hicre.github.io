# Kakashi Hicre — Portfolio

A single-page developer portfolio built with semantic HTML5, hand-written CSS3 (custom properties, no framework), and a small amount of vanilla JavaScript. No build step, no dependencies — open `index.html` in a browser or deploy directly to GitHub Pages.

## Structure

```
portfolio/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── script.js
├── assets/
│   ├── images/
│   │   └── profile/     ← add a profile photo / OG image here if you'd like one
│   ├── icons/            ← add assets/icons/favicon.svg here for the browser tab icon
│   └── cv/
│       └── Kakashi-Hicre-CV.pdf   ← add your CV here (both CV buttons already link here)
└── README.md
```

## Before you publish — placeholders to fill in

A few pieces of information weren't supplied, so they're clearly marked in the code rather than invented:

| Item | Where | What to do |
|---|---|---|
| CV file | `assets/cv/Kakashi-Hicre-CV.pdf` | Add the actual PDF at this exact path — the "View CV" and "Download CV" buttons already point here. |
| LinkedIn URL | Hero, Contact, Footer (marked `.is-placeholder`, dashed underline) | Search each file for `is-placeholder` and replace the `href="#"` with your real LinkedIn URL. |
| Internship dates | Experience section | Replace `[Add dates]` in `index.html` with the actual start/end dates. |
| Live demo links | Project cards | Each project has a disabled "Live Demo" button. Once a project is deployed, swap it for a normal `<a class="btn btn--outline btn--sm" href="...">Live Demo</a>`. |
| Favicon | `assets/icons/favicon.svg` | Optional — add a small square SVG/PNG here, or remove the `<link rel="icon">` tag in `index.html`. |
| Profile / OG image | `assets/images/profile/` | Optional — the hero deliberately uses a code-snippet visual instead of a photo since none was supplied; add one if you'd like a personal photo somewhere on the page. |

Per-project GitHub links use your general profile URL (`https://github.com/Kakashi-Hicre`) as a placeholder — point each "View Code" button at the specific repository once it exists.

## Features

- Fully responsive: desktop, laptop, tablet, and mobile layouts (not just a shrunk desktop view)
- Accessible: semantic landmarks, visible focus states, skip link, `aria-*` on the nav and disabled elements, respects `prefers-reduced-motion`
- Light/dark theme toggle, persisted in `localStorage`, with a polished (not simply inverted) dark palette
- Sticky navigation with scroll-aware styling and active-section highlighting
- Mobile hamburger menu (vanilla JS, no dependencies)
- Categorized skills, rich project cards, and an experience/education timeline

## Deploying to GitHub Pages

1. Push this folder to a GitHub repository (as the repo root, or a `/docs` folder).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set the source to the branch/folder containing `index.html`.
4. Save — GitHub will publish the site at `https://<your-username>.github.io/<repo-name>/`.

## Browser support

Uses standard modern CSS (custom properties, `color-mix()`, `clamp()`, `dvh` units) and vanilla JS (`IntersectionObserver`). Works in current versions of Chrome, Firefox, Safari, and Edge.
