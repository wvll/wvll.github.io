# WVLL 2026 Conference Website

Static site for the **2026 International Conference on Vision, Language & Learning (WVLL)** hosted at the University of North Texas (Dec 18-19, 2026). The repository also contains the archived **WVLL 2024** workshop site under `/2024`.

## Project Structure
- `/index.html` — 2026 home page with in-page sections (about, speakers, organizers, program committee, DEI, requirements, previous editions).
- `/about`, `/organizers`, `/program`, `/social_impact`, `/sponsors` — section-specific standalone pages for 2026, sharing global styles.
- `/assets` — shared images and `main.css` styling.
- `/2024/...` — archived WACV 2024 workshop site (left untouched for historical reference).

## Local Preview
No build step required. Serve the root folder with any static file server:
```bash
cd /Users/rabby/Desktop/wvll.github.io
python3 -m http.server 8000
# then open http://localhost:8000
```
Opening `index.html` directly in a browser also works, but a server is recommended for consistent relative paths.

## Editing Guidelines
- **Typography/Layout:** Global text styles live in `assets/main.css`. The 2026 home page also has inline styles near the top of `index.html`.
- **Navigation:** Desktop and mobile nav are defined in `index.html`; links should match section IDs or full URLs. “Previous Editions” intentionally points to `https://wvll.github.io/2024/`.
- **Banner details:** Title and date/location are in the `.banner` block of `index.html`.
- **Copy updates:** Prefer editing the section HTML directly. Keep paragraphs justified (set in `assets/main.css`).
- **Logos:** Logo strip containers exist but are currently empty; add `<img>` tags under `.logos` as needed.

## Deployment
Designed for GitHub Pages (or any static host). No build artifacts; publish the repository root.

## Maintenance Checklist
- Update dates, venue, and links if the conference details change.
- Add/remove speaker and committee entries in the relevant sections.
- Keep the archive under `/2024` unchanged unless intentionally revising historical content.
- When adding assets, place them in `/assets` and reference with relative paths.

## Support
For content or style changes, edit the HTML/CSS directly. No external dependencies or tooling are required beyond a basic static server for preview.

Maintainer: [Shahariar Rabby](https://rabby.dev)

