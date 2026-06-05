---
name: porters-value-chain
description: Use when analyzing where competitive advantage or margin comes from — running a Porter's Value Chain breakdown of a company OR one of the user's own software/app projects. Triggers on "value chain", "competitive advantage", "where's the margin", "strategy breakdown", or mapping a product's activities to find strengths/threats.
---

# Porter's Value Chain Analysis

Apply Michael Porter's Value Chain framework to find where competitive advantage
and margin are created — for an external company or one of the user's own
software projects.

## How to run an analysis

Follow these steps in order. Announce: "Using the Porter's Value Chain skill."

### Step 1 — Identify the target
Determine what is being analyzed.
- **User's own project:** gather context from the repo and conversation
  (README, product docs, recent commits, known collaborators). Do not ask the
  user for facts you can read yourself.
- **External company:** ask the user for what they know. Do NOT fetch financials
  or invent figures — work only from provided/known information, and flag
  assumptions explicitly.

### Step 2 — Pick the mode (ask up front)
Ask the user which lens to use:
- **Classic** — the literal nine Porter activities, force-fitting the target and
  marking any activity N/A where it does not apply.
- **Software-adapted** — Porter's structure translated for software/app/indie
  projects. Use the translation table in `references/translation-table.md`.

Do not assume — ask, even for an obviously-software target, because the user
wanted to choose each time.

### Step 3 — Map the activities into a matrix
Produce a Markdown table with one row per activity (primary first, then
support), columns:

| Activity | Cost drivers | Current state | Competitive-advantage potential |
|---|---|---|---|

Fill every cell. Use "N/A — <reason>" rather than leaving blanks.

### Step 4 — Render the value-chain diagram
Draw the classic shape inline as ASCII/Markdown: support activities as
horizontal bands across the top, primary activities as the left-to-right arrow
of boxes, and **Margin** on the right. Use this template, relabeling the primary
boxes for Software-adapted mode:

```
┌─────────────────────────────────────────────────────────────┐
│ Firm Infrastructure                                          │\
│ Human Resource Management                                    │ \
│ Technology Development                                       │  >  M
│ Procurement                                                  │ /   A
├──────────┬──────────┬──────────┬──────────────┬─────────────┤/    R
│ Inbound  │Operations│ Outbound │  Marketing   │  Service    │  >  G
│Logistics │          │ Logistics│   & Sales    │             │ /   I
└──────────┴──────────┴──────────┴──────────────┴─────────────┘     N
```

Offer an HTML/SVG version only if the user asks.

### Step 5 — Strategic synthesis
Identify the **2-3 activities** that are the real source of, or biggest threat
to, competitive advantage / margin. For each, give a one-line rationale and a
**concrete, prioritized next action**. This is the payoff — never skip it.

## Deliverable
By default, print matrix + diagram + synthesis in chat. Then offer to save a
Markdown artifact, suggesting a consistent path like
`docs/strategy/<target>-value-chain.md`. Save only if the user agrees.

## Teaching mode

If the user is asking to *learn* the framework rather than analyze a specific
target (e.g. "explain Porter's value chain", "what is the value chain"), skip
the workflow above. Instead:

1. Explain primary vs. support activities and the concept of margin.
2. Walk one short worked example (pick a familiar company or, if the user has an
   active project, theirs) through 2-3 activities.
3. Offer to run a full analysis next.

Keep it concise — this is an explainer, not a full mapping.
