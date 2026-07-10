# The PMM Signal Pack

**Six Claude skills built for Claude Fable 5.**

For the evidence-heavy side of product marketing: reading everything you already
have and pulling the signal out of it. These skills are designed to run on Claude
Fable 5, whose 1M-token context window can hold your entire evidence base in a
single run - the one job that makes this kind of large-scale synthesis possible.
Each skill also carries a fallback for everyday models (see below).

Where the [Product Marketing Skills Pack](https://github.com/pmalliance/product-marketing-skills)
helps you **produce** - positioning docs, battlecards, launch plans - this pack
helps you **see**. Each skill points at a pile of raw material you never have
time to read across (call transcripts, reviews, competitor pages, your own live
copy) and returns a structured, sourced read of it.

## Why these are Fable-recommended

Every skill in this pack does the same kind of work: hold a large body of
evidence in view at once and reason across all of it. That is the job Claude
Fable 5 is built for - a 1M-token context window means it can take your whole
evidence base in a single run and cross-reference it, instead of you feeding it
in chunks and losing the thread.

Fable is more expensive and slower than an everyday model, so these are the jobs
you reach for a few times a quarter, not every day. **Every skill also carries a
fallback:** if Fable isn't available or the budget is spent, run it on your
everyday model in batches and merge the partial results. You lose some cross-set
nuance, keep the method.

## Included Skills

| Skill | Purpose |
| --- | --- |
| `win-loss-reasons` | The real reasons you win and lose - what buyers said vs what the pattern shows, ranked, cited to the calls |
| `objection-library` | Every buyer objection, in their words, ranked by frequency and tagged to funnel stage |
| `message-consistency-check` | Where your core message says different things across your live surfaces |
| `positioning-map` | The whole competitive field side by side - crowded claims and unclaimed angles |
| `claim-check` | Every claim in your messaging checked against your evidence; flags the ones running on faith |
| `customer-language-bank` | The exact words buyers use, ranked, mapped against your current copy |

## The shared standard

Every skill holds the same rule: **every finding points back to the exact place
in your material it came from.** A reason, an objection, a claim verdict, a
buyer phrase - each cites the transcript line, review, or page behind it. If it
can't be traced to the evidence, it doesn't go in the output as a finding. That
is what separates this from "AI wrote me a doc."

## How it works

1. Gather your evidence for the job (each skill lists what to collect).
2. If you use the Product Marketing Skills Pack, its
   `.agents/product-marketing-context.md` is read first for ICP, competitors, and
   positioning. If you don't have one, the skill asks for the essentials.
3. Run the skill. Point it at your material.
4. You get a structured, sourced report you can take into a review.

## Using With Claude

### Claude Cowork / Claude Desktop / Claude Code

Drop the skill folders into your skills directory (the same place your other
skills live). Claude detects them automatically - no configuration.

### Claude.ai Projects

Upload `CLAUDE.md` and the packaged `.skill` files from `.claude/skills` into
your project.

## Repository Layout

- `skills/` - editable source for each skill (one folder per skill, each with a
  `SKILL.md`)
- `.claude/skills/` - packaged `.skill` files ready to ship
- `.claude/.claude-plugin/plugin.json` - Claude plugin metadata
- `.agents/product-marketing-context.md` - shared context template
- `CLAUDE.md` - repo-level operating instructions for Claude
- `LICENSE` - MIT

## Notes for maintainers

- This repo ships 6 skills. If you add more, update `README.md`, `CLAUDE.md`, and
  `.claude/.claude-plugin/plugin.json` together.
- A `.skill` file is just a zip of a skill's folder. Re-pack after editing any
  `SKILL.md`.
- Skills are model-agnostic. The Fable recommendation is guidance in each skill,
  not a hard dependency.
