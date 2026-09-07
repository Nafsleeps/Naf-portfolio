# Naf-portfolio

My personal portfolio — web design and AI agent services.

A single static page: `index.html` plus assets. No framework, no build step for
the HTML, and the only JavaScript is a small inline script that validates the
contact form.

## Structure

```
index.html              the page — hero, story, services, work, contact
src/styles.css          Tailwind source; the design system lives at the top
assets/styles.css       compiled stylesheet (committed — the page loads this)
assets/work/site-0*.svg work screenshot placeholders
assets/og-image.png     social share image placeholder (1200×630)
assets/favicon.svg      favicon placeholder
assets/apple-touch-icon.png
```

## Placeholders to swap before launch

Everything below is a stand-in. Search `index.html` for `PLACEHOLDER` to find
each one in place.

| What | Where | Swap in |
|---|---|---|
| Work screenshots | `assets/work/site-01.svg` … `site-04.svg` | Real screenshots. Keep the 3:2 shape, or the cards will crop them. Update the `src` and `alt` on each `<img>` in the work section. |
| Site names | Work section — `Site name 01` … `04` | The real business names. |
| Type labels | Work section — `Restaurant website`, `Repair shop website`, `Cafe website`, `Salon website` | What each project actually was. |
| Form endpoint | `<form action="https://formspree.io/f/YOUR-FORM-ID">` | Your real endpoint. Formspree, Web3Forms and Netlify Forms all take a plain POST like this one. |
| Email address | `mailto:you@example.com`, contact section | Your real address. |
| WhatsApp number | `https://wa.me/61400000000` | Your number in full international form — no `+`, no spaces. `61` is Australia, so a `04xx` mobile becomes `614xx`. |
| Domain | `<link rel="canonical">`, `og:url` | Your real URL, with the trailing slash. |
| OG image | `assets/og-image.png`, referenced absolutely in `og:image` and `twitter:image` | A real 1200×630 image. The URL must stay absolute or link previews will not load it. |
| Favicon | `assets/favicon.svg` | Your own mark. |
| Touch icon | `assets/apple-touch-icon.png` | A 180×180 PNG. |

## Design system

Defined once in the `@theme` block of `src/styles.css`; everything else inherits it.

| | |
|---|---|
| Background | `#0D0C0B` off-black |
| Text | `#EDEAE5` off-white, `#8B8781` grey for secondary |
| Accent | `#D85A30` coral — buttons and invalid fields |
| On accent | `#4A1B0C` |
| Links / hover | `#F0997B` |
| Body | 18px / 1.6 |
| H1 | 56px desktop, 36px mobile |
| Measure | 680px content, 1100px work grid |
| Section rhythm | 120px desktop, 64px mobile |

Two type sizes only (18px body, 14px labels and captions) and two weights only
(regular 400, medium 500). Motion is limited to hover, focus and field states.

## Development

```sh
npm install
npm run dev     # rebuild assets/styles.css on change
npm run build   # minified build — run before committing CSS changes
```

Then open `index.html` in a browser, or serve the directory with any static server.

## Status

All five sections are built. Checked at 375px and 1440px. The page is ready to
go live once the placeholders above are swapped.
