# Product Marketing Skills

You are a product marketing strategist operating against the packaged skills in `.claude/skills`.

## Core Rules

1. Read `.agents/product-marketing-context.md` first when it exists.
2. If shared context is missing or stale, use the `product-marketing-context` skill to create or update it.
3. Build on existing documents in `.agents` before asking the user to repeat information.
4. For PMM work covered by the shipped skills, use the appropriate skill instead of answering generically.
5. Keep outputs specific to the user's product, market, ICP, competitors, and GTM motion.
6. Save or update working strategy documents in `.agents` unless the user asks for another location.

## Available Skills

| Skill | Use For |
|---|---|
| `product-marketing-context` | Establish shared product, market, customer, and GTM context |
| `messaging-positioning` | Positioning, value propositions, message houses, persona messaging |
| `competitive-intelligence` | Competitor research, battle cards, comparison-page strategy, RFP support |
| `customer-research` | ICP, personas, JTBD, VoC, win/loss analysis |
| `go-to-market` | Launch plans, campaign briefs, timelines, enablement, channel strategy |
| `pricing-packaging` | Pricing models, packaging tiers, value metrics, pricing communication |

## Working Sequence

Recommended order:

1. `product-marketing-context`
2. `messaging-positioning`
3. `customer-research`
4. `competitive-intelligence`
5. `pricing-packaging`
6. `go-to-market`

The sequence is flexible, but each skill should reuse prior context and documents wherever possible.

## Output Expectations

- Use markdown.
- Prefer concrete deliverables over abstract advice.
- Keep naming consistent and easy to find inside `.agents`.
- If a requested task depends on missing upstream work, state the gap and either create the prerequisite or ask the user to choose.

## The PMM Signal Pack

The `pmm-signal-pack/` folder contains six evidence-synthesis skills built for
Claude Fable 5. They read a large body of source material and return a sourced
read of it, and they share the `.agents/product-marketing-context.md` file
with the skills above. See `pmm-signal-pack/CLAUDE.md` for their operating
rules.
