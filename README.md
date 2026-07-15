[README.md](https://github.com/user-attachments/files/30051655/README.md)
# WhatsApp No-Photo Snake ID — Prototype

Guided species identification for when there's no usable photo (SnakeIQ Story #2). A menu-driven WhatsApp-style dialog narrows a snake to a ranked candidate list using one shared logic engine. Region: **Gauteng**.

### ▶ [Open the live demo](https://ryan-g0.github.io/WhatsApp-No-Photo-ID-Prototype/)

The landing page links to three versions showing how the ID logic grows:

| Version | Adds | Link |
|---|---|---|
| **1 — Marais matrix only** | Morphology: size, shape, colour, pattern, behaviour, standout tells | [open](https://ryan-g0.github.io/WhatsApp-No-Photo-ID-Prototype/marais-only.html) |
| **2 — Marais + responder** | Ecology / circumstance: what you were doing, time of day, bite marks | [open](https://ryan-g0.github.io/WhatsApp-No-Photo-ID-Prototype/marais-responder.html) |
| **3 — Marais + responder + syndromic** | Envenomation-syndrome checklist + bite/spit triage gate | [open](https://ryan-g0.github.io/WhatsApp-No-Photo-ID-Prototype/marais-responder-syndromic.html) |

### How it works

Each version runs the same engine: a **species × trait matrix** (graded likelihoods, not yes/no) scored against a **regional prior**, updated Bayesian-style with every answer. An **information-gain** picker chooses the next question so the dialog never asks something it can't use, and it always returns a ranked list with honest confidence — never a dead end. The right-hand panel shows the engine's live candidate ranking and reasoning.

Safety is asymmetric by design: while any dangerous species stays plausible, the "treat as venomous" guidance shows regardless of the top pick. In v3, a reported bite always runs a fixed syndrome checklist and never de-escalates.

### Notes

- The WhatsApp frame is a **mockup of the interaction model**, not a live bot.
- Trait data is drawn from Johan Marais / African Snakebite Institute material for common Gauteng species.
- The syndrome layer is **decision-support, not diagnosis** — it needs clinical sign-off before any real-world use.
