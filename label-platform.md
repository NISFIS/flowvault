# FlowVault → Label Platform (product concept + validation plan)

*How the consumer FlowVault app evolves into a B2B platform sold to record labels — using a "free for the artist, paid for the organization" (product-led / bottom-up) model.*

**Status:** concept & validation plan. Nothing here is built yet. This is the thinking to validate *before* writing app code — same fake-door discipline as the existing FlowVault landing page.

---

## 1. The product in one sentence

FlowVault is a genuinely useful, **free** songwriting tool for artists (bars, lyrics, projects, voice memos). A **paid management layer** sits on top, sold to the **label/manager**, giving them big-picture visibility and control over every artist's project status — and consolidating that work into the company's cloud.

Analogy: *Asana/Monday, but built for how a label actually makes records* — and with a free artist-facing tool as the adoption engine (the way Slack/Notion/Figma spread bottom-up).

## 2. The two layers (and who pays)

| Layer | For whom | Price | Value delivered |
|---|---|---|---|
| **FlowVault (base)** | The artist | **Free** | Real writing tool: bars/lyrics library with tags, projects, voice-memo → text. Must be excellent on its own. |
| **Management + company cloud** | The label / manager | **Paid** | Portfolio-level view of every artist's songs and their status; centralized, backed-up company cloud; oversight without micromanagement. |

**Why this split is honest (value-first):** the free layer has real value for the artist, and the paid layer has real value for the organization. Neither is an artificial paywall on something worthless. A paywall without value just creates churn.

## 3. Who pays vs. who uses — and why both matter

- **Buyer = label / A&R / manager.** They pay for *the big picture*: which song is at which stage, which project is behind, portfolio health at a glance.
- **Users = artists + producers.** They do the actual creative work in the tool.

**The critical dependency:** if artists and producers don't use the free tool, the label's dashboard is empty — and there's nothing to sell. Adoption of the free layer is the prerequisite for monetizing the paid layer. This is the whole engine.

## 4. The wedge — the FIRST paid feature to build

"A complete platform to run a label" is the long-term vision, **not** the first product. Start with ONE feature that the label will pay for. Proposed wedge:

> **A song/release status board.** The label sees every artist's tracks moving through defined stages — e.g. *Idea → Writing → Demo → Recording → Mixing → Mastering → Released* — plus who's stuck and what's overdue, in one view. Backed by the company cloud so nothing lives only on an artist's phone.

Why this wedge:
- It's exactly the "big-picture management" pain the concept is built around.
- It's only valuable *because* artists are using the free tool underneath — so it reinforces the adoption engine.
- It's narrow enough for a solo/small builder to ship well, and it's the natural seed for later modules (contracts, royalties, release scheduling, collaboration with the label's producers).

**Guardrail (keep it value-aligned):** "moving a project into the company cloud" must give the *artist* value too — collaboration with the label's producers, real backups, cross-device sync — not just surveillance. When both sides benefit, the model is durable.

## 5. Go-to-market sequence — bottom-up, small → big

The architecture dictates the order. You cannot cold-sell a major label with an empty product.

1. **Get artists using free FlowVault.** This is also your first, most important validation: does anyone actually use it?
2. **Sell the management layer to whoever manages those artists** — start with **indie/small labels and artist managers** (a handful of artists each). They feel the same pain, but are reachable and fast to close, with far less bureaucracy than majors.
3. **Grow into larger labels** once you have usage + proof. Big labels are the *destination*, not the starting point.

## 6. Validation plan (fake-door, before building)

Validate **both sides** before writing app code — reuse the existing FlowVault landing-page pattern.

**Side A — do artists actually use the free tool?**
- The current FlowVault fake-door (landing page → waitlist) already tests artist demand. Interpret its go/no-go numbers first (see `plan.md`).

**Side B — would a label/manager pay for the management layer?**
- A second, separate landing page aimed at **indie labels / managers**: "See every artist's tracks and their status in one place — and your artists actually use it."
- CTA = "Book a demo" / waitlist, not a real paywall. Collected emails/booked calls = genuine willingness-to-pay signal, with nothing worthless paywalled.
- Optionally: a "Pro / company cloud — coming soon, ~€X/mo, want early access?" button inside the free app once it exists, routing to a waitlist. This is the honest "day one" price signal.

**Decision rule:** only build the paid management layer once (a) artists demonstrably use the free tool, AND (b) at least a few small labels/managers signal they'd pay. Both, not either.

## 7. Open questions to resolve next

- **Competitive landscape:** what do Splice, BandLab, Soundcharts, generic Notion/Asana, and existing label-management tools *not* do? (Hypothesis: none connect the artist's creative work + the label's oversight in one place.)
- **First-customer profile:** which exact indie label / manager archetype is easiest to reach and feels the pain most?
- **Pricing shape:** per-artist seat, flat per-label, or usage/storage-based for the company cloud.
- **Artist trust:** how to keep the "artist-made, not corporate" FlowVault brand so artists adopt willingly — this brand is a real competitive asset against corporate-feeling incumbents.
