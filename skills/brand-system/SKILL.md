---
name: brand-system
description: >
  A brand system encoded as a skill. Apply any time the request involves producing a
  branded artefact — documents, decks, one-pagers, proposals, web pages, emails, social
  tiles, internal memos, anything carrying the brand's name. The brand vocabulary is
  small (one accent colour, two typefaces, one mark, restraint) and the compositional
  possibilities are enormous. Read this skill, internalise the DNA, then design freely
  with full creative ambition per context.
---

# {{BRAND_NAME}} — Brand Skill

## Read this first

You're producing something for {{BRAND_NAME}} — [one-line description of the company and
its posture]. Your job is to make it **genuinely beautiful**. Not just on-brand. Not just
compliant. **Beautiful.** A document that someone wants to share, screenshot, hold onto.

The brand DNA is small:

- **{{BRAND_ACCENT}}** — one accent colour, used surgically as a wayfinding accent
- **{{DISPLAY_FONT}}** (display) + **{{BODY_FONT}}** (body)
- **The mark** — the logo, also usable as a graphic device
- **Restraint** — confident whitespace, near-black ink, white or dark canvases
- **A plain, direct voice** — see `voice/voice-guide.md`

That's it. Within that DNA, the compositional possibilities are enormous. Reach for them.

## Why this is a skill and not a PDF

Brand guidelines are written for humans who will interpret them. A skill is written for a
model that will *execute* them — and the two need different things.

A PDF can say "use the brand thoughtfully." A skill can't. Vagueness produces one of two
failure modes, and you will hit both before you get this right:

1. **Too prescriptive** → the model reimplements your rules literally and the output is
   plain. Correct-looking, lifeless. Nobody wants to share it.
2. **Too loose** → the model invents, and you get gradients, glows, six colours, and
   marketing-speak.

The resolution is a **small set of hard rules plus explicit creative permission**. Constrain
the atoms tightly. Leave composition wide open. Then show, with real reference outputs, what
the ceiling looks like — because a model calibrates against examples far better than against
adjectives.

## What good looks like

Put two or three real, finished reference outputs in `examples/` and point at them here.
This is the highest-leverage part of the entire skill.

This repo ships two, both real outputs from the studio this skill was built at, sanitised
for public release (see `examples/README.md`):

- `examples/em-capability-onepager.html` — a single dark-canvas capability page: one
  confident typographic moment, a stat row, a selected-work list.
- `examples/em-proposal-baycare.html` — a four-page client proposal (fictional client):
  cover, editorial opportunity page, a structural phases/scope grid, and a pricing +
  signature page. Pricing figures are redacted.

Note how differently the two compose while holding the same DNA — that contrast is the point.

**Reference outputs beat rules.** A single well-composed example moves output quality more
than fifty lines of instruction, because it sets the ceiling rather than the floor. Without
them, "beautiful" is an adjective the model has to guess at.

Pick examples that solve *different* design problems — a cover, a structural page, a
decision page — so it's obvious that composition varies by context while the DNA holds.

## The mindset that produces good work

**Design per context, don't template.**

A capability one-pager wants a different composition than a proposal cover, which wants a
different composition than a pricing page. Each page has a job. Each composition should
serve that job.

- **Cover pages** want one confident moment — usually a typographic statement
- **Editorial reading pages** want long-form layout — multi-column text, pull-quotes
- **Structural pages** (scope, phases, deliverables) want grids and modular components
- **Decision pages** (pricing, terms, signature) want maximum clarity — restrained, table-like

There is no single template. There is the DNA, applied per context with full design intelligence.

**Restraint is the default, ambition is the move.**

Most of any page is white, ink, or dark canvas. The accent colour shows up as one word in a
headline, one CTA, one stat suffix — surgical and meaningful. When the accent is everywhere,
it stops being meaningful.

But restraint is not caution. The cover headline can be 76pt. The dark panel can take half a
page. The pull-quote can break the column. **Be ambitious within the restraint.**

## Suggested structure

```
brand-system/
├── SKILL.md            ← you are here
├── tokens/             ← the atoms: colours, typography, spacing
├── voice/              ← how the brand speaks (the half everyone skips)
├── devices/            ← compositional possibilities, not requirements
├── modes/              ← engineering rules per output context (print vs screen)
├── logos/              ← every mark variant as SVG
├── examples/           ← THE BAR. Real finished outputs.
└── reference/          ← pre-ship checklist
```

Two notes from practice:

- **`voice/` matters as much as `tokens/`.** Most brand systems encode the visual half and
  leave voice implicit. The result is artefacts that look right and read wrong.
- **`devices/` must be framed as *possibilities*, not *requirements*.** Label it explicitly.
  Otherwise the model treats the device list as a checklist and every page gets a pull-quote.

## The few hard rules

Keep this list short. Everything not on it is craft, judgement, and creative permission.

1. **Use only the canonical palette** in `tokens/`. Don't invent brand colours.
2. **Use only the two canonical typefaces.**
3. **No gradients.** Flat colour reads as more confident.
4. **No drop shadows on type, no glow on logos.** The brand reads as serious because it
   doesn't try too hard.
5. **Body text is the ink colour.** Never the accent, never grey.
6. **The mark appears at least once per document.**
7. **Restrained accent.** Surgical only. Never large fills or tinted card backgrounds.
8. **End client-facing documents with a contact block.**

## After producing the asset

1. Run `reference/checklist.md`.
2. If the output is going to a real client, state explicitly: *"Drafted, not sent — needs
   review before going out."*
3. Open it in a browser or render to PDF and visually verify the first page. Do not declare
   done on unrendered code.

## A note on under-shooting

If the output looks plain — a corporate document with brand colours applied — you've
under-shot. The DNA is *restraint*, not *blandness*. Restraint means surgical accent,
near-black ink, generous whitespace. It does not mean white-page-with-thin-cards.
