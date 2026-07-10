# Product Marketing Skills

Six packaged Claude skills for core product marketing work: context setup, messaging, competitive intelligence, customer research, go-to-market planning, and pricing.

These skills live in `.claude/skills` as packaged `.skill` files and share a common context file at `.agents/product-marketing-context.md`.

## Included Skills

| Skill | Purpose |
|---|---|
| `product-marketing-context` | Creates and maintains the shared PMM context file |
| `messaging-positioning` | Builds positioning, value props, message houses, and persona messaging |
| `competitive-intelligence` | Produces competitor analysis, battle cards, and comparison-page inputs |
| `customer-research` | Develops ICP, personas, JTBD, VoC, and win/loss insights |
| `go-to-market` | Plans launches, campaigns, timelines, enablement, and cross-functional GTM execution |
| `pricing-packaging` | Recommends pricing models, tiers, value metrics, and pricing-page guidance |

## How It Works

1. Start with `product-marketing-context`.
2. Save shared context in `.agents/product-marketing-context.md`.
3. Run the specialized skills as needed. They should read the context file first and only ask for missing task-specific details.
4. Save strategy docs and working outputs in `.agents` unless your workflow requires another location.

## Repository Layout

- `.claude/skills`: packaged skill files used by Claude
- `.claude/.claude-plugin/plugin.json`: Claude plugin metadata
- `.agents/product-marketing-context.md`: shared PMM context file
- `CLAUDE.md`: repo-level operating instructions for Claude
- `my-gtm-context.md`: reference template

## Using With Claude

### Claude Code / Claude Desktop

Open this repository as your working directory. Claude can use the packaged skills from `.claude/skills` directly.

### Claude.ai Projects

Upload:

- `CLAUDE.md`
- The packaged `.skill` files from `.claude/skills`
- Optionally `.agents/product-marketing-context.md` if you want to preload context

Do not look for unpacked `SKILL.md` folders in this repo. The shipped artifacts are the `.skill` packages themselves.

## Recommended Workflow

1. Create or update product context.
2. Define messaging and positioning.
3. Run customer research and competitive intelligence.
4. Build pricing and packaging guidance.
5. Turn that strategy into a GTM plan.

## The PMM Signal Pack

Built for Claude Fable 5. Six skills for the evidence-heavy side of product
marketing - reading everything you already have and pulling the signal out of
it. Where the skills above help you produce (positioning, messaging,
competitive, research, pricing, GTM), the Signal Pack helps you see: point it
at your call transcripts, reviews, competitor pages, and your own copy, and it
returns a structured, sourced read of it. Fable 5's 1M-token context window can
hold your whole evidence base in a single run, which is what these jobs need.
Each skill also carries a fallback for everyday models.

- `win-loss-reasons` - the real reasons you win and lose, what buyers said vs
  what the pattern shows, ranked and cited to the calls
- `objection-library` - every buyer objection, in their words, ranked by
  frequency and tagged to funnel stage
- `message-consistency-check` - where your core message says different things
  across your live surfaces
- `positioning-map` - the whole competitive field side by side, crowded claims
  and unclaimed angles
- `claim-check` - every claim in your messaging checked against your evidence,
  flagging the ones running on faith
- `customer-language-bank` - the exact words buyers use, ranked, mapped against
  your current copy

To install: download this repo, then drop the `pmm-signal-pack` folder into
your Claude skills directory. Full details in `pmm-signal-pack/README.md`.

## Notes

- This repo ships 6 PMM skills.
- Use `.agents/product-marketing-context.md` for shared context.
- If you add more skills later, update `README.md`, `CLAUDE.md`, and `.claude/.claude-plugin/plugin.json` together.
