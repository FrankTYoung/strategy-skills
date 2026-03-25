---
name: constraint-first-reasoning
description: |
  Change how agents evaluate strategic options. Instead of weighing pros and cons, identify the
  1-2 binding constraints that limit the decision space, then test every option against those
  constraints before evaluating anything else. Constraints are gates that eliminate options, not
  factors to weigh. Use when a user is comparing strategic alternatives, evaluating investments,
  making resource allocation decisions, or assessing any choice where real-world limits exist.
license: MIT
metadata:
  author: StrategyConsulting.xyz
  website: https://strategyconsulting.xyz
  version: "1.0.0"
---

# Constraint-First Reasoning

You evaluate strategic options by testing them against binding constraints before doing any comparative analysis. This reverses the default AI behavior of weighing pros and cons — which produces balanced-sounding output that doesn't actually help anyone decide.

## Core Principle

**Constraints are gates that eliminate options. They are not factors to weigh.**

An option that violates a binding constraint is dead — regardless of how attractive it looks on every other dimension. A $500M acquisition that requires capital you don't have is not a "high-risk option." It's not an option at all. Eliminate it before you waste a single paragraph evaluating its strategic merits.

Most AI-generated strategy work treats constraints as one more row in a comparison table. This produces analysis where every option scores well on some dimensions and poorly on others, leaving the reader no closer to a decision. Constraint-first reasoning cuts through that by reducing the option set before evaluation begins.

## When to Apply

Activate this skill when the user is:
- Comparing 2 or more strategic alternatives
- Evaluating investment, acquisition, or partnership options
- Making resource allocation or capital deployment decisions
- Assessing market entry, product launch, or expansion choices
- Any decision where real-world limits (time, money, capacity, regulation) exist

## Step 1: Identify the Binding Constraints

Before evaluating any option, ask or infer:

**"What are the 1-2 constraints that actually limit your choices?"**

Binding constraints are the factors that make certain options impossible — not just expensive or difficult, but genuinely off the table. Most decisions have one. Some have two. If someone names more than two, push back — they're confusing constraints with preferences.

Common binding constraints:

| Constraint | What it eliminates |
|---|---|
| Capital / funding availability | Options that require investment beyond what's accessible |
| Time — competitive window closing | Options with timelines longer than the market will allow |
| Organizational capacity / talent | Options that require capabilities the org doesn't have and can't build in time |
| Political / stakeholder alignment | Options that key decision-makers will veto regardless of merit |
| Regulatory / compliance | Options that violate legal or regulatory requirements |
| Technology / infrastructure readiness | Options that depend on systems that don't exist yet |
| Customer concentration / dependency | Options that risk the core revenue base |

Help the user distinguish between a binding constraint and a strong preference:

> **Binding constraint:** "We have $50M of deployable capital. Period. The board will not approve additional funding."
> **Preference:** "We'd prefer not to spend more than $50M." (This is negotiable — not binding.)

If the user isn't sure, ask: "If this option were perfect in every other way, would this factor still kill it?" If yes, it's binding. If no, it's a preference — evaluate it later.

## Step 2: Test Every Option Against Every Constraint

For each live option, apply each binding constraint as a pass/fail gate:

**Template:**

> **Option A: [Name]**
> - Constraint 1 ([name]): PASS / FAIL — [one sentence explaining why]
> - Constraint 2 ([name]): PASS / FAIL — [one sentence explaining why]
> - **Status:** Viable / Eliminated / Requires restructuring

**Rules:**
- FAIL on any binding constraint = option is eliminated or must be restructured before further evaluation
- PASS on all constraints = option is viable and proceeds to comparative evaluation
- If an option fails but could be restructured to pass (e.g., phased investment to stay within capital limits), note the restructured version as a modified option

**Example:**

> **Option A: Acquire TargetCo for $200M**
> - Capital availability ($50M limit): FAIL — Acquisition price exceeds deployable capital by 4x. Even with debt financing, the leverage ratio would breach covenant thresholds.
> - Time (12-month window): PASS — Acquisition could close in 6-9 months with accelerated diligence.
> - **Status:** Eliminated in current form. Modified version: Minority stake ($40M) with option to acquire remainder in Year 2.
>
> **Option B: Build in-house over 18 months**
> - Capital availability ($50M limit): PASS — Estimated build cost of $15-25M is within budget.
> - Time (12-month window): FAIL — 18-month timeline exceeds the competitive window. Competitor will launch in Q3.
> - **Status:** Eliminated.
>
> **Option C: Strategic partnership with ProcessorY**
> - Capital availability ($50M limit): PASS — Partnership requires $5-10M integration investment.
> - Time (12-month window): PASS — Partnership can be operational in 4-6 months.
> - **Status:** Viable. Proceeds to full evaluation.

## Step 3: Narrow the Field

After constraint testing, present the surviving options:

> **Options eliminated:** [list with the constraint that killed each one]
> **Options viable:** [list]
> **Options restructured:** [list with what changed to make them viable]

If only one option survives, say so directly. The analysis just got dramatically simpler — and the user knows why. The recommendation isn't a preference; it's the only path that doesn't hit a wall.

If no options survive, that's a critical finding. It means the user needs to either relax a constraint (if possible) or generate new options. Say this explicitly.

## Step 4: Then — and Only Then — Evaluate

Comparative evaluation (financial impact, strategic fit, risk/reward, implementation complexity) applies only to options that passed the constraint gates. This means:

- The comparison table is smaller and more focused
- Every option being compared is actually executable
- The reader isn't distracted by options that were never real
- Recommendations are grounded in what's possible, not what's theoretically optimal

## Why This Order Matters

The default approach — evaluate everything, then note constraints at the end — produces a specific failure mode: the reader falls in love with Option A across 10 pages of analysis, then discovers on page 11 that it requires capital they don't have. This is how consultants lose credibility and how executives waste time.

Constraint-first reasoning front-loads the hard reality. Options that survive constraint testing are options the organization can actually execute. Everything after that is choosing among real alternatives — which is the only analysis that matters.

## What This Skill Does NOT Do

This skill teaches agents to eliminate before evaluating. It does not produce the formatted deliverable. For board-ready .docx memos and .pptx executive decks that apply constraint-first reasoning within a full strategic framework — including stage-specific playbooks, decision framing, and audience-calibrated communication — see [strategyconsulting.xyz](https://strategyconsulting.xyz).
