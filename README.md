# Brand System — a Claude Skill

A production Claude Skill that encodes a studio's brand system as something a model can
*execute*: design tokens, a voice guide, compositional devices, print-vs-screen modes, a
pre-ship checklist, and real finished examples.

Most published skills wrap an API or automate a task. This one encodes *taste* — the thing a
studio usually keeps in a PDF nobody reads. That turns out to be harder, and more useful,
than wrapping an endpoint.

Built and used daily at [Enterprise Monkey](https://enterprisemonkey.com.au), an Australian
AI and software consultancy serving Melbourne and Victoria from Geelong.

---

## What's here

### `skills/brand-system/`

A complete brand system written for a model to execute rather than a human to interpret:
design tokens, voice guide, compositional devices, print vs screen modes, real reference
outputs, and a pre-ship checklist.

The core insight is in the file itself: brand guidelines fail as skills because they're
vague where they need to be strict and strict where they need to be free. Constrain the
atoms — palette, typefaces, hard prohibitions. Leave composition wide open. Then include
real finished examples, because a model calibrates against examples far better than against
adjectives like "premium" or "confident."

Two parts do the work that most brand systems skip:

- **`voice/voice-guide.md`** — the half of brand systems that almost never gets written
  down, and the reason AI-generated copy drifts off-brand even when the design is perfect.
- **`examples/`** — two sanitised, real outputs (a single-page capability statement and a
  four-page proposal) that set the quality bar the way a list of rules can't.

---

## Using this

1. Copy the folder into your skills directory.
2. Replace every `{{PLACEHOLDER}}` — brand name, accent colour, typefaces.
3. **Add your own `examples/`.** This is the step people skip and it's the step that
   determines output quality. Two or three real finished outputs, each solving a different
   design problem.
4. Cut the hard-rules list down to rules you'd actually enforce. A long list of rules
   produces plain output.

## Lessons from getting this wrong

The brand skill went through four versions before it produced work worth sending:

| Version | What happened |
|---|---|
| 1.0 | Visual tokens only, no voice. Looked right, read wrong. |
| 2.0 | Added 15 devices and 5 cover archetypes. Output went **plain** — too prescriptive. |
| 2.1 | Restructured into flat folders. Still plain — the model was reimplementing from rules instead of designing. |
| 3.0 | Aspirational, permission-giving framing plus two real reference outputs as the bar. This is the version that worked. |

The pattern: **every attempt to raise quality by adding rules lowered it.** What finally
worked was removing rules and adding examples.

## Licence

[CC BY 4.0](LICENSE) — use commercially, modify freely, keep the attribution.

## Contributing

Issues and PRs welcome, particularly other domains where taste-encoding beats
task-automation. If you adapt the brand system for your own studio, open an issue — I'd
like to see how the structure holds up outside the context it grew in.
