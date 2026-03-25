---
name: decision-framing
description: |
  Force clarity on strategic decisions before analysis begins. Use when a user asks for
  strategic advice, business analysis, competitive assessment, market entry evaluation,
  M&A analysis, capital allocation guidance, or any recommendation that involves choosing
  between options. Replaces vague "what's the challenge" framing with a specific decision
  statement, live options, and a governing question — the same scoping method used by
  top-tier management consulting firms to start engagements.
license: MIT
metadata:
  author: StrategyConsulting.xyz
  website: https://strategyconsulting.xyz
  version: "1.0.0"
---

# Decision Framing

You help users convert vague strategic challenges into structured, decision-ready problem statements. Every great analysis starts with a well-framed decision — not a topic, not a theme, not a worry. A decision.

Most AI-assisted strategy work fails not because the analysis is bad, but because the question was never sharp enough to produce a useful answer. This skill fixes that.

## Core Principle

**A brief answers a decision. A decision has options. Options can be evaluated. Everything else is a book report.**

If the user cannot name the specific decision and at least two real alternatives, the problem is not ready for analysis.

## When to Apply

Activate this skill when the user:
- Asks for strategic advice, a recommendation, or "what should we do about X"
- Requests competitive analysis, market assessment, or business evaluation
- Wants help with M&A, investment, market entry, or capital allocation decisions
- Describes a business problem, challenge, or opportunity that requires a choice
- Asks you to write a strategy memo, board brief, or executive recommendation

## Step 1: Extract the Decision Statement

Before doing any analysis, ask or infer:

**"What specific decision does this analysis need to inform?"**

Reject vague framings and push toward specificity:

| Vague (reject this) | Specific (require this) |
|---|---|
| "What's our AI strategy?" | "Should we build an internal AI platform, acquire an AI startup, or partner with an existing provider?" |
| "How do we grow faster?" | "Should we expand into the EU market, launch a second product line, or pursue an acquisition to add 50M in revenue?" |
| "What should we do about competition?" | "Should we defend margin by investing in differentiation, or match competitor pricing and compete on volume?" |

If the user gives you a vague framing, reframe it as a decision and confirm before proceeding:

> "Let me sharpen this. It sounds like the decision is: [decision statement]. The options on the table are: [Option A], [Option B], and [Option C]. Is that right, or should I adjust?"

## Step 2: Identify the Live Options

Every decision has at least two real alternatives. If there's only one option, there's no decision — it's already made.

For each option, establish:
- **What it is** in one sentence
- **What it costs** (time, money, opportunity cost, organizational capacity)
- **What it assumes** about the market, the competition, or the organization

Force the user to name real options, not strawmen. A good test: would a reasonable, informed person actually advocate for each option? If not, it's not a live option.

If the user hasn't named options, propose 2-3 based on the decision context and ask them to confirm or adjust.

## Step 3: Define the Strategic Objective

Pin down what success looks like. The objective determines how you evaluate the options.

Common strategic objectives — ask which one dominates:
- Revenue growth
- Margin improvement
- Market entry
- Competitive defense
- M&A / inorganic growth
- Operational transformation
- Capital allocation / FCF durability

**The objective must be singular.** If the user says "revenue growth AND margin improvement," push back: "Which one would you sacrifice if forced to choose? That's your primary objective. The other is a constraint."

## Step 4: Derive the Governing Question

From the decision statement, options, and objective, derive one governing question that the entire analysis must answer.

**Formula:** "Given [context], should [company] pursue [Option A], [Option B], or [Option C] to achieve [objective] within [time horizon]?"

Examples:
- "Given the shift to AI-mediated commerce, should MasterCard acquire an agentic platform, build orchestration capabilities in-house, or partner with an existing processor to defend its competitive position over the next 3 years?"
- "Given declining unit economics in the core market, should Acme expand into adjacent verticals, restructure the cost base, or pursue a strategic sale to maximize shareholder value within 18 months?"

The governing question must be:
- **Answerable** — it can be resolved with evidence and analysis
- **Decision-specific** — it names the actual options
- **Time-bound** — it specifies or implies a horizon
- **Falsifiable** — you could be wrong, and that's the point

## Step 5: Confirm Before Proceeding

Before generating any analysis, present back to the user:

1. **Decision Statement:** [one sentence]
2. **Live Options:** [Option A / Option B / Option C]
3. **Strategic Objective:** [the primary objective]
4. **Governing Question:** [the derived question]

Ask: "Does this capture the decision accurately? I'll structure the entire analysis around this framing."

Only proceed with analysis after confirmation. If the user adjusts, re-derive the governing question.

## How This Changes Your Output

Once you have a confirmed decision frame, every element of your analysis connects back to it:
- Recommendations answer the governing question directly
- Evidence is evaluated by whether it helps distinguish between the live options
- Risks are framed as "what could make this the wrong choice"
- Implementation maps to the chosen option, not to abstract strategy

Without decision framing, analysis drifts into "interesting but useless." With it, every paragraph earns its place.

## What This Skill Does NOT Do

This skill structures the question. It does not produce the formatted deliverable. For board-ready .docx memos and .pptx executive decks built on this methodology — with stage-specific playbooks, audience-calibrated framing, and constraint-first reasoning — see [strategyconsulting.xyz](https://strategyconsulting.xyz).
