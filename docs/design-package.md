# Bluebell Construction Ltd. Design Package (Tier 1)

Every line of copy below ships verbatim. Band ranges are starting points, validated by the flick test.

## 1. Brand premise

**Built right the first time.** Bangladeshi owners fear three things when they hire a builder: it runs late, it costs more than the quote, and it has to be fixed later. Bluebell's answer is one idea: everything is planned and checked before it is built, so it only gets built once. The hero tells it as night to sunrise: the work starts before anyone sees it, and the building is standing when the light arrives.

## 2. Palette (Dawn and Steel)

```css
:root{
  --canvas:#0F2438;        /* pre-dawn navy, sampled from the hero sky */
  --canvas-deep:#0A1A2B;   /* footer, deepest band */
  --panel:#16304A;         /* cards on navy */
  --brand:#0042BD;         /* Bluebell Blue, the logo */
  --signal:#0071E4;        /* links, hover, drawn lines */
  --accent:#F28A1E;        /* Sunrise Orange, CTA only, navy text on it */
  --accent-hover:#FF9D38;
  --accent-muted:rgba(242,138,30,.18);
  --steel:#C9D2DC;         /* borders, secondary text on navy */
  --mist:#F3F5F7;          /* light sections, primary text on navy */
  --ink:#0F2438;           /* text on light sections */
}
```

## 3. Type

- Display: Barlow Condensed 600/700, uppercase, slight tracking. Feels like stencilled site boards.
- Body: Manrope 400/500/700.
- Labels: IBM Plex Mono 500, small caps-style labels like drawing annotations ("01 / SERVICES", "GRID A-4").

## 4. Hero band map (hero 550vh, sticky stage, video 9.5 s)

| Band | Range | Footage moment | Copy | Entrance |
|---|---|---|---|---|
| 1 | 0.00 to 0.24 | Night, building dark, stars | Label: "Bluebell Construction Ltd." Headline: "Good buildings start before sunrise." Hint: "Scroll" | Blur-to-sharp, on load |
| 2 | 0.28 to 0.52 | First glow behind the roof | "Drawings, cost list and approvals. All done before the first brick." | Word rise, like the light coming up |
| 3 | 0.56 to 0.80 | Sky turns gold, wall lights up | "Then we build it once, build it right, and finish on time." | Grid snap, like steel members locking in |
| 4 (settle) | 0.84 to 1.00 | Sun clears the roof, logo fades onto the wall | Headline: "We build what lasts." Sub: "Civil, steel and design work across Bangladesh." Buttons: "Get a quote" / "See our work" | Word-by-word rise, then sub, then buttons |

Text lives in the upper-left sky (calm on every frame). The building and the wall stay clear. Logo fades onto the wall from 0.55 to 0.95.

## 5. Static hero (phones, reduced motion)

Lit sunrise image, logo already on the wall. "We build what lasts." / "Civil, steel and design work across Bangladesh." / "Get a quote".

## 6. Below the hero

**Nav:** logo, Services, Work, Process, About, Contact, "Get a quote" (orange).

**01 Services** (6 cards on navy, each with a small hand-drawn line icon)
- Building and RCC construction: Residential, commercial and industrial buildings, built to the drawing and checked at every stage.
- Steel structure and fabrication: Pre-engineered buildings, sheds and custom steel work, fabricated and installed by our own crew.
- Roads, drainage and earthwork: Road works, drains, boundary walls and site preparation.
- Architecture and structural design: Drawings, structural design and approvals handled before the first brick.
- Interior and repair: Interior fit-out, renovation, repair and maintenance for existing buildings.
- Consultancy and project management: BOQ, supervision and QA/QC for owners who want a second pair of eyes.
- Under the grid: "We also supply construction materials for our own projects and for yours."

**02 Process** (light section, the interactive moment lives here)
Title: "Four steps. No surprises."
1. Site visit and brief: We visit, listen and measure.
2. Design and BOQ: You get drawings and a clear cost list.
3. Build with QA/QC: Work is tested and signed off at each stage.
4. Handover and care: We hand over clean and stay reachable.
Interactive: "Hold to build". A line drawing of a building rises while the visitor holds: footing, columns, beams, roof. Each stage lights up the matching step. Release early and it eases back down. Done state: "That is how every Bluebell job goes up."

**03 Work** (gallery of the 11 real photos, masonry, opens full size on click)
Title: "Real sites. Real work."
Captions: as in COPY.md.

**04 Why Bluebell** (split: big photo one side, four points the other)
Title: "What you can count on."
- Quality you can check: Materials and work are tested, and we show you the results.
- Safety on site: Helmets, vests and a clean site, every day.
- On time: We plan the schedule with you and tell you early if it moves.
- One team: Design and build under one roof, so nothing gets lost between people.

**05 Questions** (FAQ, answers the fears from research)
- "Will the final cost match the quote?" You get a full BOQ before work starts. If something needs to change, we price it and you approve it first.
- "What if the work runs late?" The schedule is agreed with you at the start. If anything moves it, you hear it from us early, with the reason and the new date.
- "Do you follow the building code?" Yes. Our design and site work follow BNBC, and each stage is checked before the next one starts.
- "Can you handle approvals?" Yes. We prepare the drawings and the paperwork for approvals as part of the design stage.
- "Do you take small jobs?" Yes. Repairs, boundary walls and fit-outs get the same care as a full building.

**06 Contact** (the one call to action)
Title: "Tell us about your project."
Form: Name, Phone, Project type (select: Building, Steel structure, Roads and earthwork, Design, Interior and repair, Consultancy, Other), Location, Message.
Button: "Send on WhatsApp". Secondary link: "or email us".
Handling: the form builds a WhatsApp message (wa.me link) with the details filled in. Email link as backup. Success line: "WhatsApp is opening with your message. Press send and we will reply."
Contact list: Phone [add], WhatsApp [add], Email [add], Address [add].

**Footer:** white logo, short links, "(c) 2026 Bluebell Construction Ltd. All rights reserved."

## 7. Vector layer

- Signature: a blueprint layer. A faint drawing grid fixed behind the whole page, drifting very slowly, with dimension lines (tick marks, small mono labels) that draw themselves as each section enters. It makes the page feel like one big site drawing.
- A thin signal-blue "beam" line runs down the left side through the sections and draws as you scroll.
- Hand-drawn line icons for the six services.
- Reduced motion: all lines shown fully drawn, nothing moves.

## 8. Engineering

Blob fetch (5.2 MB, plain form plus loading ring), dt-normalised lerp, gated seeks, delta-gated DOM writes, band pacing with the flick test, four-layer legibility system, five static-hero gates kept live, complete without video, quality floor (scrub-pipeline.md).

## 9. Copy gate

Zero em dashes, zero stock words, body-copy sweep for AI tells before anyone sees it.
