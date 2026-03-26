# Strategy Skills — Installation Guide

Three consulting-grade skills that teach AI agents how top-tier strategy firms actually scope work. Built by [strategyconsulting.xyz](https://strategyconsulting.xyz).

| Skill | What It Does |
|-------|-------------|
| **decision-framing** | Forces vague questions into specific decisions with named options |
| **constraint-first-reasoning** | Eliminates options against binding constraints before evaluating |
| **audience-calibrated-communication** | Calibrates recommendations to the audience that needs to act |

---

## Prerequisites

- A Claude account (Free, Pro, Max, Team, or Enterprise)
- **Code execution and file creation** enabled in your Claude settings
- Basic comfort with downloading files and navigating settings menus

---

## Step 1 — Download the Skills

Go to the GitHub repository:

```
https://github.com/FrankTYoung/strategy-skills
```

Click the green **Code** button → **Download ZIP**. Unzip the file on your computer. You'll see three folders:

```
strategy-skills/
├── decision-framing/
│   └── SKILL.md
├── constraint-first-reasoning/
│   └── SKILL.md
├── audience-calibrated-communication/
│   └── SKILL.md
├── LICENSE
└── README.md
```

Each skill is a self-contained folder with a single `SKILL.md` file inside it.

---

## Step 2 — Choose Your Installation Surface

These skills work across three Claude surfaces. Pick the one you use.

---

### Option A: Claude.ai (Web / Mobile App)

This is the simplest path. No code required.

1. **Enable Code Execution**
   - Go to **Settings → Capabilities**
   - Toggle on **Code execution and file creation**

2. **Zip each skill folder individually**
   - You need one `.zip` file per skill
   - On Mac: right-click the folder → Compress
   - On Windows: right-click → Send to → Compressed (zipped) folder
   - Example: `decision-framing.zip`, `constraint-first-reasoning.zip`, `audience-calibrated-communication.zip`

3. **Upload each skill**
   - Go to **Customize → Skills** (or **Settings → Features**, depending on your plan)
   - Click the upload area and select your `.zip` file
   - Repeat for each skill you want to install

4. **Verify**
   - Each skill should now appear in your Skills list with a toggle
   - Make sure each toggle is **on**
   - Ask Claude: *"What skills are available?"* — it should list them

5. **Test it**
   - Try: *"Help me think through whether we should build, buy, or partner for our payment orchestration layer."*
   - Claude should automatically invoke the decision-framing skill to sharpen the question before diving into analysis.

---

### Option B: Claude Code (Terminal / CLI)

If you use Claude Code for development or agentic work:

1. **For personal (global) skills — available in every project:**

   ```bash
   # Create the skills directory if it doesn't exist
   mkdir -p ~/.claude/skills/

   # Copy each skill folder
   cp -r strategy-skills/decision-framing ~/.claude/skills/
   cp -r strategy-skills/constraint-first-reasoning ~/.claude/skills/
   cp -r strategy-skills/audience-calibrated-communication ~/.claude/skills/
   ```

2. **For project-level skills — available only in a specific project:**

   ```bash
   # From your project root
   mkdir -p .claude/skills/

   cp -r strategy-skills/decision-framing .claude/skills/
   cp -r strategy-skills/constraint-first-reasoning .claude/skills/
   cp -r strategy-skills/audience-calibrated-communication .claude/skills/
   ```

3. **Verify**
   - In Claude Code, ask: *"What skills are available?"*
   - Or invoke directly: `/decision-framing`

---

### Option C: Claude API

For programmatic access via the Anthropic API:

1. **Upload each skill** using the Skills API endpoint:

   ```bash
   curl -X POST "https://api.anthropic.com/v1/skills" \
     -H "x-api-key: $ANTHROPIC_API_KEY" \
     -H "anthropic-version: 2023-06-01" \
     -H "anthropic-beta: skills-2025-10-02" \
     -H "content-type: application/json" \
     -d '{
       "name": "decision-framing",
       "description": "Force clarity on strategic decisions before analysis begins.",
       "source": {
         "type": "directory",
         "path": "./strategy-skills/decision-framing"
       }
     }'
   ```

   Repeat for each skill. Note the `skill_id` returned in each response.

2. **Use skills in API calls** by referencing them in the `container` parameter:

   ```bash
   curl https://api.anthropic.com/v1/messages \
     -H "x-api-key: $ANTHROPIC_API_KEY" \
     -H "anthropic-version: 2023-06-01" \
     -H "anthropic-beta: code-execution-2025-08-25,skills-2025-10-02" \
     -H "content-type: application/json" \
     -d '{
       "model": "claude-sonnet-4-6",
       "max_tokens": 4096,
       "container": {
         "skills": [
           {
             "type": "custom",
             "skill_id": "YOUR_SKILL_ID_HERE",
             "version": "latest"
           }
         ]
       },
       "messages": [{
         "role": "user",
         "content": "Should we build or acquire a stablecoin settlement capability?"
       }],
       "tools": [{
         "type": "code_execution_20250825",
         "name": "code_execution"
       }]
     }'
   ```

---

## How the Skills Work Together

These skills are designed to chain naturally. You don't need to invoke them manually — Claude will recognize when each one applies:

1. **Decision Framing** fires first when you bring a vague strategic question. It forces specificity: what's the decision, what are the live options, what's the governing question.

2. **Constraint-First Reasoning** kicks in during evaluation. Instead of weighing pros and cons (which produces fence-sitting), it identifies binding constraints and eliminates dead options before analyzing survivors.

3. **Audience-Calibrated Communication** shapes the output. A skeptical CFO gets risk and unit economics up front. A board that's already aligned gets execution specificity. An investment committee gets thesis validation and return scenarios.

You can also invoke any skill explicitly by name if Claude doesn't auto-detect the right context.

---

## Troubleshooting

| Problem | Fix |
|---------|-----|
| Skill doesn't trigger | Check that it's toggled **on** in your Skills list. Try invoking it by name. |
| Skill triggers when it shouldn't | This is rare with these skills since they have specific descriptions, but you can toggle off any skill you don't want active. |
| "No skills found" | Make sure Code execution is enabled. Re-upload the zip. |
| Claude Code doesn't see the skill | Confirm the folder is in `~/.claude/skills/` (global) or `.claude/skills/` (project) and contains `SKILL.md`. |

---

## What These Skills Don't Do

These skills structure the *thinking* — they don't produce formatted deliverables. For board-ready `.docx` memos and `.pptx` executive decks built on this methodology, visit [strategyconsulting.xyz](https://strategyconsulting.xyz).

---

## License

MIT — use freely, modify as needed, attribution appreciated.

## Questions?

Open an issue on the [GitHub repo](https://github.com/FrankTYoung/strategy-skills) or reach out via [strategyconsulting.xyz](https://strategyconsulting.xyz).
