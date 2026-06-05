# Porter's Value Chain — Claude Skill

A [Claude Code](https://claude.com/claude-code) skill that applies Michael
Porter's **Value Chain** framework to find where competitive advantage and
margin are created — for an external company **or** one of your own software
projects.

## What it does

When invoked, the skill drives a five-step analysis:

1. **Identify the target** — a company, or one of your own projects (it pulls
   context from your repo where it can).
2. **Pick a mode** (asked up front):
   - **Classic** — the literal nine Porter activities.
   - **Software-adapted** — Porter's structure translated for software/app
     projects (e.g. *inbound logistics → data/content & API pipelines*,
     *operations → dev & infra*, *service → support & retention*).
3. **Activity matrix** — each activity scored on cost drivers, current state,
   and competitive-advantage potential.
4. **Value-chain diagram** — the classic support-bands-over-primary-arrow shape,
   rendered inline.
5. **Strategic synthesis** — the 2–3 activities that are the real source of (or
   biggest threat to) advantage/margin, with concrete prioritized next actions.

It also has a lightweight **teaching mode** for "just explain the framework"
requests.

## Example output

A run on a fictional habit-tracking app (illustrative):

![Example value-chain analysis for a fictional app](assets/example-analysis.png)

## Install

Clone into your Claude Code skills directory:

```bash
git clone https://github.com/InfiniteInsight/PortersValueChain-ClaudeSkill \
  ~/.claude/skills/porters-value-chain
```

Then restart Claude Code. The skill auto-registers and triggers on phrases like
"value chain", "competitive advantage", "where's the margin", or "strategy
breakdown".

> Note: the install path must be `~/.claude/skills/porters-value-chain` (the
> folder name should match the skill's `name`).

## Files

```
porters-value-chain/
├── SKILL.md                        # the skill: trigger + workflow
├── references/
│   └── translation-table.md        # software-adapted activity lenses
└── assets/
    └── example-analysis.png        # example output (for the README)
```

## Usage

Just ask, e.g.:

- "Run a Porter's value chain on Notion."
- "Do a value-chain breakdown of my project to find where the margin is."
- "Explain Porter's value chain." *(teaching mode)*

## License

MIT
