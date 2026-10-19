# Bluebell Construction Ltd. website

The website for **bluebellconstructionltd.com**. Civil, steel and design work across Bangladesh.

Plain HTML, CSS and vanilla JavaScript. One `index.html` plus `assets/`. No framework, no build step.

## What is in here

| Path | What it is |
|---|---|
| `index.html` | The whole site: markup, styles and scripts |
| `assets/hero.mp4` | The scroll hero: night to sunrise over a steel shed (9.5 s, keyframe every 2 frames for smooth scrubbing) |
| `assets/hero-poster.jpg`, `hero-mobile.jpg`, `hero-poster-lit.jpg` | Hero stills: first frame, lit ending (phones and reduced motion), share image |
| `assets/logo/` | Logo files (blue, white, icon), favicon and touch icons |
| `assets/img/` | Real project photos from Bluebell sites |
| `docs/` | The design plan and the original brief and copy |

## How the hero works

Scrolling through the hero scrubs the video. The logo is mapped onto the shed door with a `matrix3d` transform built from the door's four measured corners, so it keeps the door's perspective at any screen size. Phones and visitors with reduced motion get a still sunrise image instead of the video.

## Before going live

Fill in the real contact details:

- In `index.html`, the `WHATSAPP` and `EMAIL` constants at the top of the script.
- The `[add ...]` placeholders in the Contact section.
- The `og:image` and `og:url` tags marked `DEPLOY STEP` in the head, with the live absolute URL.

## Run it locally

```
npx http-server -p 8080 .
```

Then open http://localhost:8080. Opening `index.html` directly shows the still hero, because browsers block the video fetch on `file://`.
