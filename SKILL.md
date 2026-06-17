---
name: globant-frontend-design
description: Build production-grade frontend interfaces in Globant's design language — the "Green Book" brand. A signature bright-green palette (spring/mint through lime) used as gradient accents over a white-predominant canvas, near-black text, a bold modern sans-serif, the forward-pointing arrow motif, and delightful motion ("technology that dares to delight"). Use whenever the user wants a UI, web page, component, dashboard, landing page, app screen, or marketing site to look like Globant, "Globant brand", the "Green Book", "Globant green", a green-gradient aesthetic, or a bold, optimistic, forward-moving tech-consultancy look. Defaults to React; also supports framework-free HTML/CSS and any framework via the shared CSS tokens. Trigger even when the user names a framework (React, Angular, Vue) but wants the Globant look, and even if they never say "Globant" but describe a bright-green, gradient-accented, white-predominant, delight-driven interface.
---

# Globant Frontend Design

This skill produces frontend interfaces that look and feel like they belong to Globant's brand world — the visual system documented in Globant's public brand portal (the **"Green Book"**). The output should read as authentically Globant: confident and optimistic, built on a **white-predominant canvas** with **near-black text**, **bright-green gradient accents** as the signature flourish, a **bold modern sans-serif**, the **forward-pointing arrow** as a recurring motif, and motion that earns the tagline *"technology that dares to delight."*

The user provides a UI to build: a component, page, dashboard, landing page, or app. They may name a framework, point to a Globant property to emulate, or just say "make it look like Globant." Your job is to pick the right stack, apply the design system faithfully, and execute the details that separate an authentic Globant interface from a hollow "neon green on white" imitation.

## The core tension to manage

Globant's brand is built on a very bright, almost electric green — and bright green is the easiest thing in the world to misuse. Lazy "Globant" looks like a screen flooded with `#25F198` buttons, neon text that fails contrast, and rainbow gradients everywhere. **Authentic Globant is restrained**: green is a *device*, not a *fill*. What makes a UI read as genuinely Globant:

- **White predominates.** This is the single most important rule in the Green Book. The canvas is white (or near-white) and calm. Green is the accent that punctuates it — a gradient hero band, a CTA, an underline, a data highlight, an icon — never the dominant surface across the whole screen.
- **Green lives mostly in gradients.** The brand's signature is the green gradient (spring → mint → lime, or spring → teal). Gradients are a *complement* used to reinforce branding, applied to hero backgrounds, key callouts, and accent shapes — not splashed onto every element. A flat solid-green button is fine for one primary CTA; ten of them is slop.
- **Near-black text, never green text on white.** Bright green has terrible contrast on white. Body and headings are near-black (`#111`) on white; green is reserved for large fills, gradient surfaces, dark-background moments, and non-text accents. When green meets text, the text sits on a dark or green surface, not the other way around.
- **The arrow / forward motion.** Globant's pictogram is an arrow pointing right — momentum toward the future. Echo it: rightward chevrons on links and CTAs, a slide-right on hover, diagonal motion, a sense of forward lean in the layout.
- **Bold, modern, slightly extended display type.** Headlines are heavy and confident with generous tracking; body is a clean, legible sans. Real weight contrast between the two.
- **Delight in the details.** The brand promise is *daring to delight* — so include considered micro-interactions: a gradient that shifts on hover, an arrow that slides, a reveal on scroll, a glow on a primary action. One or two well-made moments, not gratuitous animation.
- **Generous, confident whitespace.** A 4px-based grid, clear hierarchy, room to breathe. The energy comes from the green and the type, so the layout itself stays composed.

Commit to the system fully. A faithful Globant interface is bold and energetic *because* it's disciplined — the bright green earns its impact by being rare.

## Step 1 — Choose the stack

Pick based on what the user said. Globant is a digital-engineering firm that builds in everything, so there's no single "native" framework the way Angular is native to Google — **default to React**, which is the most broadly useful and renders cleanly as a self-contained artifact.

| Signal from the user | Stack | Reference |
|---|---|---|
| "React", "Next", a React codebase, or nothing specified | React (single-file or project) | `references/react.md` |
| "plain HTML", "no framework", "vanilla", a single-file artifact, an email, or a static page | HTML + CSS custom properties | `references/vanilla.md` |
| "Angular", "Vue", "Svelte", or another framework | That framework, consuming `assets/tokens.css` | `references/vanilla.md` (token usage is framework-agnostic) |

**Always read `references/design-tokens.md` regardless of stack** — it defines the palette, gradients, type scale, shape, spacing, elevation, and motion that every path shares. Then read the chosen stack reference for setup and copy-paste-ready patterns.

If you're producing a self-contained artifact (claude.ai) and the user didn't demand a specific framework, prefer the **vanilla** path or a **single-file React** path — they render without a build step.

## Step 2 — Apply the design system

1. Read `references/design-tokens.md` for the shared palette, gradients, and scales, plus the exact color-discipline rules.
2. Read the stack reference for the wiring.
3. Use the bundled asset as your starting point rather than re-deriving tokens:
   - `assets/tokens.css` — the full Globant token set as CSS custom properties (green palette, gradients, neutrals, type scale, radii, spacing, shadows, motion), ready for the vanilla path or any framework that reads CSS variables.
4. Build the actual interface. Wire up real interactions, real state, real content. No lorem-ipsum-and-gray-boxes mockups unless the user explicitly asks for a wireframe.

## Step 3 — Get the signature details right

Before finishing, check the interface against the things that make it *Globant*. Exact values live in `references/design-tokens.md`; the headline checklist:

- **Canvas:** white / near-white dominates; the screen feels calm and open, not green-saturated.
- **Green as accent:** at least one signature green-gradient moment (hero, callout, or accent shape); solid green reserved for a single primary CTA or key highlight. Verify green is never carrying small text on a white background.
- **Type:** bold, slightly extended display headings with real tracking, set against a clean legible body sans; weight contrast is obvious (e.g., 700/800 display vs 400 body). Sizes are multiples of 4.
- **Arrow / momentum:** the forward-arrow motif appears somewhere (link chevron, CTA, hover slide, diagonal accent) and the layout has a forward lean.
- **Motion:** at least one considered, brand-appropriate interaction using the easing tokens — a gradient shift, an arrow slide, a scroll reveal, a CTA glow.
- **Contrast & accessibility:** near-black on white for text; white or near-black on green/gradient surfaces; confirm pairs meet WCAG AA.
- **Spacing:** a 4/8px grid with the generous, confident whitespace the brand is known for.

## Color discipline (the rule that makes or breaks it)

From the Green Book, in priority order:

1. **White predominates.** If you removed all color, the layout should still be ~70%+ white/neutral.
2. **Green and gradients are a complement**, used to reinforce branding — heroes, CTAs, highlights, icons, accent shapes. Not a background for entire content sections of text.
3. **Don't overload secondaries.** A single composition uses one or two greens plus a gradient, not the whole ramp at once.
4. **Don't distort the colors** — no blend modes or effects that shift the brand hues; no muddy overlays on the green.

`references/design-tokens.md` gives the gradient recipes and the safe text/surface pairings.

## Fonts

Globant's wordmark uses a **bespoke custom typeface** that isn't publicly distributable, so — exactly like defaulting to Roboto when Google Sans isn't guaranteed — **substitute a close, freely available modern sans** and always ship a robust fallback chain.

- **Display / headlines:** a bold, modern, slightly extended grotesque. Good free choices: **Space Grotesk**, **Archivo** / **Archivo Expanded**, or **Clash Display**. Use heavy weights (700–800) with generous letter-spacing for the confident, forward Globant voice.
- **Body / UI:** a clean, highly legible neutral sans — **Inter**, **Manrope**, or **Roboto**.
- **Code:** **JetBrains Mono** or **Roboto Mono**.
- Always end the stack in `system-ui, -apple-system, sans-serif`. Use font sizes that are **multiples of 4** (12, 16, 20, 24, 32, 36, 48, 64), matching the Green Book's scale. Exact import strings and the type scale are in `references/design-tokens.md`.

If the user supplies the actual Globant brand fonts (or the Green Book / Figma tokens), use those instead and align hexes exactly.

## On staying current

Framework versions move fast; the reference files capture current setup patterns, but if the user is on a different version or something doesn't compile, prefer the framework's own current docs over hard-coded version numbers here. The *design system* (the white-predominant canvas, the green gradients, the arrow motif, the type and motion feel) is the stable part; the wiring that delivers it is what drifts. Brand specifics can also evolve — if precise current hexes matter, confirm against Globant's brand portal.

## Quality bar

This skill is about consistency with an established, opinionated brand — but consistency is never an excuse for blandness, and *especially* not here, because Globant's whole promise is to *delight*. Match implementation effort to the surface: a landing page wants a bold gradient hero, atmosphere, and a memorable forward-leaning moment; a dashboard wants legible density with green used sparingly for highlights and status; a settings panel wants calm, white, confident clarity. Sweat the details, keep the green disciplined, and make at least one moment genuinely delightful. Someone from Globant should look at the result and recognize their own brand reflected back accurately.
