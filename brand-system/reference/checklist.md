# Pre-Ship Checklist

Run through this before declaring any EM-branded asset done. If all 8 pass, ship it.

---

## 1. Composition

- [ ] The page has one clear hero element (headline, big stat, hero photo, dark scope panel) — not five competing ones
- [ ] Composition serves the page's job (cover ≠ content ≠ pricing ≠ contact)
- [ ] Layout is appropriate for the content (editorial reading vs. modular structural vs. data-led)

## 2. Restraint

- [ ] Orange used 2-4 times across the page surface, with intent — not as decoration
- [ ] No gradients anywhere
- [ ] No drop shadows on type, no glow effects on logos
- [ ] Generous whitespace — the page doesn't feel crammed

## 3. Identity

- [ ] The C-mark appears at least once (corner mark, watermark, inline icon, process device)
- [ ] If wordmark appears, it's at minimum size (48px / 16mm) with clear space
- [ ] Logo isn't recoloured, tilted, stretched, or distorted

## 4. Colour

- [ ] Only the canonical EM colours appear (orange, ink, ink-soft, page-muted, page) plus working extensions (charcoal, soft greys, hover-state oranges)
- [ ] No invented brand colours
- [ ] Body text is `--brand-ink` (near-black), not orange, not grey
- [ ] WCAG AA contrast met (orange-on-white only for headings ≥18px)

## 5. Typography

- [ ] {{DISPLAY_FONT}} for display / headings, {{BODY_FONT}} for body — no other fonts
- [ ] Headlines in sentence case by default (lowercase only for editorial hero moments, with intent)
- [ ] Body type is at least 14px, line-height 1.5+
- [ ] Heading hierarchy is sequential

## 6. Voice

- [ ] No banned words (leverage, utilise, synergy, journey, passionate, exciting, innovative, cutting-edge, best-in-class, world-class, industry-leading, robust, seamless, frictionless, holistic)
- [ ] No corporate AI-isms (tapestry, weave, transform, unlock potential)
- [ ] Active voice predominantly
- [ ] Quotes attributed to a named human
- [ ] Australian English

## 7. Print-friendliness (if PDF / print output)

- [ ] Renders cleanly via Chrome PDF (Playwright) — WeasyPrint may not handle modern CSS reliably
- [ ] No content overflow or extra blank pages
- [ ] All SVGs inline (no broken external references)
- [ ] Page margins respected

## 8. Content accuracy

- [ ] All facts verified — no fabricated case study results, no made-up client names, no invented stats
- [ ] Any certification or compliance claim is current and verifiable
- [ ] Contact details correct (phone, email, domain)
- [ ] Founding year correct (2014)
- [ ] Headline numbers from `voice/boilerplate.md` used verbatim
- [ ] If going to a real client (not internal review), explicitly stated: "Drafted, not sent — needs review before going out"

---

## When the check fails

**Composition / Restraint** — usually means add whitespace and remove an element, not the other way round. Pull orange out, not put more in.

**Identity / Colour / Typography** — fix at the token level (CSS variables), not by overriding inline.

**Voice** — rewrite. Don't apologise for it. The brand is the writing.

**Print** — see `modes/print.css` "Print engineering — gotchas" section.

**Content** — verify, then fix. Don't guess.
