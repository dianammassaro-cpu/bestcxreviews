# CLAUDE.md

Project memory for **bestCXreviews**. Read this first.

## What we are building

bestCXreviews.com: an independent, thought-leadership publication and review site for **AI-based software that helps companies manage customer conversations**, across two modes:
1. Conversations handled by AI (chatbots, virtual agents, autonomous "AI agents").
2. Conversations handled by humans, assisted by AI (agent copilots, real-time guidance, conversation analytics, automated QA).

The editorial through-line is the convergence of those two modes. The brand's entire value is **independence and honesty in a hyped category**. Not an affiliate listicle site, not a vendor channel.

Full strategy: see `README.md`.

## Current status

- Strategy brief written (`README.md`).
- Brand identity v1.1 complete (`design/`): logo system, color, type, brand standards.
- Reference sites gathered (`research/references.md`).
- Task list at `TASKS.md`.
- **Website: launch build complete** in `site/` as plain static HTML/CSS (no build step), built from the brand system and verified in-browser. Stack is provisional, chosen for instant viewability while the owner was unavailable; Astro/Next + MDX remains an option to confirm later. Pages: home, reviews index, sample review (RTINGS-style scorecard + comparison table), analysis index, three articles (autonomy gap, containment math, copilot ROI), category map, methodology, about/independence. Shared styles in `site/css/styles.css`; logos in `site/assets/`.
- Local preview: `node serve.js` then open `http://127.0.0.1:8123` (serves `site/`).
- **Content note:** review scores and stat figures are illustrative placeholders demonstrating the format; replace with real tested data before publishing. Newsletter form is front-end only.
- **Not yet pushed to GitHub.** Repo `dianammassaro-cpu/bestcxreviews` exists but the current fine-grained token (shared with the PEP repo) lacks write access; owner is updating token access.

## Repository structure

```
bestCXreviews/
  CLAUDE.md                  <- you are here
  README.md                  <- vision, positioning, content pillars, voice
  TASKS.md                   <- running task list (update as work completes)
  design/
    tokens.css               <- design tokens as CSS vars (import into site)
    tokens.json              <- same tokens, machine-readable
    brand-standards.html     <- full brand guidelines (open in browser)
    brand-preview.png        <- one-page visual summary
    logo-primary.svg         <- wordmark, ink + emerald (light bg)
    logo-reversed.svg        <- wordmark for dark bg
    logo-mono-ink.svg        <- single-color wordmark
    monogram-dark.svg        <- CX app icon / avatar (ink tile)
    monogram-emerald.svg     <- CX app icon / avatar (emerald tile)
    build_logos.py           <- regenerates logos from fonts/
    fonts/                   <- source typefaces (Fraunces, Hanken Grotesk)
  research/
    references.md            <- curated design + content reference sites
```

## Brand quick reference

Use `design/tokens.css` (or `tokens.json`) as the single source of truth. Summary:

- **Colors:** Ink `#16191D`, Paper `#F4F0E8` (default background, warm not white), Emerald `#0F7A52` (the only UI accent, used sparingly). Neutrals: Slate `#5B6168`, Hairline `#DAD4C8`. Emerald Light `#23A877` for dark backgrounds.
- **Type:** Fraunces (display serif) for headlines and voice; Hanken Grotesk (grotesque) for body, UI, and the wordmark. Both SIL OFL.
- **Logo:** the X in CX is a two-tone crossing mark (emerald + ink strokes meeting) standing for the exchange between customer and company. Outlined SVG, font-independent. Regenerate with `python3 design/build_logos.py`.

## Voice and content rules

When writing any site copy or article content, match the brand voice:
- **Independent, always.** Recommendations defensible in public. Disclose how the site makes money.
- **Evidence over adjectives.** Claims come with receipts (transcripts, numbers, screenshots). No "best-in-class," "powerful," "revolutionary."
- **Plain-spoken.** Short sentences, real words, no buzzword soup ("agentic orchestration to optimize CX" is banned).
- **Opinionated, with reasoning shown.** Take a position; explain how you got there.

Review methodology is the trust anchor: always explain the *how* (how a verdict was reached), test hands-on, and state where each tool fails. Model on Wirecutter (the what/why/how) and RTINGS (transparent scoring). See `research/references.md`.

## Project conventions (apply to all generated content and code)

- **No em-dashes or en-dashes** anywhere in copy. Use a comma, period, parentheses, or colon. Hyphens in compound words ("well-known") are fine.
- **No generic AI design tells.** No purple/blue gradients, no glassmorphism, no everything-centered layouts. In particular, **do not put words in pills/badges** as a default styling crutch.
- Warm paper background over stark white. One disciplined accent (emerald), not a rainbow.
- Logos: never skew, recolor, add gradients/glows/shadows, or rebuild the lockup. Below ~140px wide, switch to the monogram.
- Prefer outlined SVG for brand marks so there is no font dependency.

## Decisions pending (do not assume; confirm with the owner)

- **Tech stack** for the site. Not chosen. A sensible default given the editorial + occasional-interactive needs would be Astro or Next.js with MDX for articles, but confirm before scaffolding.
- **Niche lead:** autonomous AI agents first, or full conversation stack from day one.
- **Review/testing methodology** spec (the trust anchor) is not yet written.
- Domain and social handles not yet secured.

See `TASKS.md` for the live list.
