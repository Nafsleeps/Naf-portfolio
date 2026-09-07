# Naf-portfolio

My personal portfolio — web design and AI agent services.

A single static page: `index.html` plus assets. No framework, no JavaScript.

## Structure

```
index.html          the page — five sections: hero, story, services, work, contact
src/styles.css      Tailwind source; the design system lives at the top
assets/styles.css   compiled stylesheet (committed — the page loads this)
assets/favicon.svg
```

## Design system

Defined once in the `@theme` block of `src/styles.css`; everything else inherits it.

| | |
|---|---|
| Background | `#0D0C0B` off-black |
| Text | `#EDEAE5` off-white, `#8B8781` grey for secondary |
| Accent | `#D85A30` coral — buttons, kept to ~5% of the page |
| On accent | `#4A1B0C` |
| Links / hover | `#F0997B` |
| Body | 18px / 1.6 |
| H1 | 56px desktop, 36px mobile |
| Measure | 680px content, 1100px work grid |
| Section rhythm | 120px desktop, 64px mobile |

Two type sizes only (18px body, 14px labels and captions) and two weights only
(regular 400, medium 500). Motion is limited to hover states.

## Development

```sh
npm install
npm run dev     # rebuild assets/styles.css on change
npm run build   # minified build — run before committing CSS changes
```

Then open `index.html` in a browser, or serve the directory with any static server.

## Status

The hero is built. Story, services, work and contact are stubbed containers
waiting on content.
