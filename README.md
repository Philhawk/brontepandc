# Bronte P&C website

A single, self-contained website for the Bronte Public School Parents & Citizens
Association. Built from the Claude Design prototype (`Bronte PandC Website.dc.html`).

## What it is

- **One file:** [`index.html`](index.html) — all 11 sections (Home, New Families,
  What's On, Get Involved, Services, Projects & Impact, Meetings, Donate/Sponsor,
  News, Contact, Style guide), the header/footer, mobile menu, accordions, event &
  news filters, service tabs and three forms. Vanilla HTML/CSS/JS, **no build step.**
- **`assets/bronte-crest.png`** — the school crest used in the header and footer.

Brand: Bronte Blue `#0059A8`, Deep Navy `#002B7F`, Bronte Yellow `#FFD928`,
Soft Sky `#9DC9E2`, Warm White `#FFFDF7`. Type: Fraunces (headings), Manrope
(body), Spline Sans Mono (labels/dates) — loaded from Google Fonts.

## Running / previewing locally

It's a static site, so any static server works. From this folder:

```bash
python3 -m http.server 4178      # then open http://localhost:4178
# or
npx serve .
```

(A tiny Node preview server lives in `.claude/static-server.js` for the in-app
preview; it isn't part of the deployed site.)

## Hosting

Drop `index.html` and the `assets/` folder onto any static host — GitHub Pages,
Netlify (drag-and-drop), Cloudflare Pages, or the school's existing web space.
No server-side code is required.

## What's still a placeholder (committee to fill in)

- **Photos** — every striped blue panel is an image placeholder with a caption of
  what should go there. Replace each with a real photo (or swap the placeholder
  `<div>` for an `<img>`).
- **Forms** — the Volunteer matcher, Become-a-supporter and Contact forms validate
  and show a thank-you message but **don't send anywhere yet**. Wire them to a form
  service (e.g. Formspree) or a `mailto:` handoff to `brontepandc@gmail.com` when ready.
- **Meeting documents** — the Agenda / Minutes / Actions / Meeting pack buttons in
  the meeting archive are placeholder links (`href="#"`); attach the real documents.

## Editing content

All page content lives in plain data arrays near the top of the `<script>` in
`index.html` — `EVENTS`, `PROJECTS`, `MEETINGS`, `UPDATES`, `COMMITTEE`, `SPONSORS`,
`QUICK`, etc. Add or edit an entry there and it appears on the relevant page; no
HTML surgery needed for routine updates.
