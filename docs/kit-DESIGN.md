# Bluebell Construction Ltd. – Design Package (Tier 1, single scroll journey)

Domain: bluebellconstructionltd.com (Hostinger). Stack: plain HTML + CSS + vanilla JS. One `index.html`, assets in `assets/`. No build step, no framework.

## Brand
- Colors: blue #0042BD, light blue #0071E4, dark blue #00257D, navy ink #0B1B33, off-white #F5F7FA, sunrise orange #F28A1E (accent only: buttons, small highlights, numbers)
- Fonts (Google Fonts): display = "Barlow Condensed" 600/700 (uppercase headings, construction feel); body = "Manrope" 400/500/600. Bangla text, if added later: "Noto Sans Bengali" (NEVER Hind Siliguri).
- Tone: calm, strong, plain. No em dashes anywhere. Avoid words: leverage, seamless, empower, unlock, robust, actionable, data-driven, solutions.

## Hero (the main effect)
- `assets/hero.mp4`: 1280x720, 24 fps, 228 frames, 9.5 s, no audio, keyframe every 2 frames (scrub-friendly). Static camera. Ends on lit sunrise.
- Desktop: hero section is ~400vh tall with a `position: sticky` 100vh stage. Scroll progress (0 to 1 across the hero) drives `video.currentTime = progress * duration`, smoothed with lerp in requestAnimationFrame (factor ~0.12). Fetch the mp4 as a Blob and use the object URL so seeking is instant.
- Phone / `prefers-reduced-motion`: no scrubbing. Show `assets/hero-mobile.jpg` (lit state) as a still background; the logo fades in on load.
- Logo reveal: DO NOT bake the logo into the video. Overlay `assets/logo/logo-blue-trim.png` (transparent PNG) on the blank front wall.
  - Opacity = smoothstep(progress, 0.55, 0.95). Also add `mix-blend-mode: multiply` at low opacity so it feels printed on the wall, and a very slight blur that goes 2px to 0.
  - Wall position inside the 1280x720 video frame (last frame), in % of the frame: left 35.6%, right 73.1%, top 47.2% (left) / 50.3% (right), bottom 78.5%. Logo box roughly: left 41%, width 26%, top 52%. Fine tune by eye.
  - Because the video is `object-fit: cover`, put video + logo inside one wrapper with aspect-ratio 16/9 and scale the wrapper (cover math in JS or CSS) so the logo stays glued to the wall at any screen size.
  - Slight perspective: `transform: perspective(900px) rotateY(-6deg) skewY(2.5deg)`; tune until it sits flat on the wall.
- Overlay text on hero: small label at top left ("Bluebell Construction Ltd."), headline appears near the end of the scroll (progress > 0.85) with a "Scroll" hint at the start. Headline: "We build what lasts." Sub: "Civil, steel and design work across Bangladesh."
- Dark gradient at top of the stage for navbar legibility.

## Sections (after hero)
1. Navbar (sticky, transparent over hero, solid navy after): logo-white-trim, links: Services, Projects, About, Contact, button "Get a quote" (orange).
2. Services (6 cards, navy/white): Building and RCC construction; Steel structure and fabrication (PEB, sheds); Roads, drainage, earthwork and boundary walls; Architectural and structural design; Interior design and repair; Consultancy and project management (BOQ, QA/QC) + materials supply as a line under the grid.
3. How we work: 4 steps – Site visit and brief, Design and BOQ, Build with QA/QC, Handover and care.
4. Projects: horizontal/masonry gallery using `assets/img/project-*.jpg`, unified navy tint on hover, lightbox optional. Captions in COPY.md.
5. Why Bluebell: 4 short points (quality, safety, on-time delivery, one team for design and build) with big numbers only if the owner gives real numbers. Otherwise no numbers.
6. Contact / quote: phone, WhatsApp, email, address, simple form (see below), footer with logo-white-trim.

## Form handling
Hostinger shared hosting: use a plain `mailto:`/WhatsApp link button first (zero backend). Upgrade later to Formspree or a small PHP mail script.

## Performance
- Poster = `hero-mobile.jpg` on the video element. Lazy-load project images. Images already <=1600px.
- Add meta description, Open Graph image (hero-poster-lit.jpg), favicon links, `lang="en"`.

## Open items from the owner
Phone, WhatsApp, email, address, tagline approval, whether the logo needs "Ltd.", confirmation that photos 23/19 etc. are Bluebell's own work (photos 22, 39 and 29 are NOT included on purpose), and whether to say the hero building is an illustration.
