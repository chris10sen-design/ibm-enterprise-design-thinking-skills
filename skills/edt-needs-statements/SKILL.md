---
name: edt-needs-statements
description: >-
  Write Needs Statements using IBM Enterprise Design Thinking — translates user observations, pain points,
  and research patterns into clear outcome-focused statements in the format "[user] needs a way to [do X]
  so that they [benefit in this way]". Use after any user research or Empathy Map session when the
  team is ready to frame what the user actually needs before generating ideas. Trigger on "needs statements",
  "what do our users need", "write user needs", "frame the need", "define user needs", "user needs",
  "how do we turn research into needs", "needs before ideation", "reframe as a need", "user need statement",
  "what problem are we solving", "frame the problem", "turn observations into needs", "design challenge",
  "how might we", "user outcome".
metadata:
  display_name: EDT Needs Statements
  short_description: Translate user research and observations into outcome-focused Needs Statements
  author: Jan Christensen
  version: "0.1"
---

# Needs Statements

A Needs Statement translates what you observed about a user into a clear, actionable target for design.
The format is deliberate:

> **[User] needs a way to [do X] so that they [benefit in this way].**

The "so that" clause is the most important part. It forces the team to focus on the user's outcome — not
the product's feature. If the statement reads naturally without the "so that" clause, it's describing a
feature, not a need. Rewrite it.

**When to use it:**
- After an Empathy Map session when patterns are clear enough to frame what the user needs
- After an As-Is Scenario Map when lows and gaps have been identified
- When the team is about to start ideation and needs a shared problem statement to generate ideas against
- When stakeholders are pushing for solutions before the problem is framed

**Time:** 20–30 minutes

---

## Step 0 — Choose your mode

Before starting, ask:

> *"Do you want to work through your research together and I'll help you derive the needs — or do you already have an Empathy Map, scenario map, or notes you'd like me to turn into Needs Statements?"*

- **Facilitate mode** → agent asks structured questions to draw out observations, then helps the team write and refine statements
- **Synthesize mode** → user shares existing material; agent writes the Needs Statements directly

---

## Facilitate Mode

### Step 1 — Ground in observations

Ask:

> *"Before we write the needs, let's anchor in what you actually observed. What are the biggest pain points or moments of frustration you saw? What are users struggling to do, or doing in a workaround way?"*

Capture the observations. Push for specifics — "users can't find X" is better than "navigation is confusing."

If the team has already run an Empathy Map or As-Is Scenario Map, ask them to share the lows and gaps
from that output. Those are the primary inputs for Needs Statements.

### Step 2 — Diverge on needs

For each significant observation or pain point:

> *"Based on what you saw — what does [user] need in this part of their experience? Try writing 2–3 versions. Use the format: '[user] needs a way to [do X] so that they [benefit].' Push past the obvious ones."*

Encourage quantity before quality. Capture everything without evaluating.

### Step 3 — Apply the "so that" test

Review each draft statement. For each one, read it aloud without the "so that" clause.

- If it still reads as a complete, sensible statement → it's probably a feature, not a need. Ask: *"What would completing this do for the user?"* and rewrite.
- If it feels incomplete without the "so that" → it's likely framed as a genuine need.

Common rewrite pattern:

| Draft (feature) | Rewritten (need) |
|---|---|
| Alex needs a dashboard | Alex needs a way to see the status of all active jobs at a glance so that they can respond to failures before users are affected |
| The user needs notifications | Sam needs a way to know when a process completes without watching it so that they can focus on other work |

### Step 4 — Converge on the strongest

Review all statements together:

> *"Which 3–6 represent the most important things to solve? Look for:*
> *- Needs that are grounded in multiple observations*
> *- Needs connected to the strongest emotional signals*
> *- Needs where you have real evidence from research, not just assumptions"*

Refine the final set. Each statement should be specific enough to guide ideation but open enough not to
prescribe a solution.

---

## Synthesize Mode

Ask the user to share their material:

> *"Paste in your Empathy Map, scenario map notes, or research observations — as raw or structured as you have it. I'll derive the Needs Statements from what you share."*

Once you have the input:

1. **Extract pain points and gaps** — identify moments of frustration, confusion, failure, or friction in the material; gaps where the user's goal is blocked or unclear
2. **Draft Needs Statements** — for each significant pain point or gap, write 1–2 statements in the format `[user] needs a way to... so that they...`
3. **Apply the "so that" test** — verify every statement has an outcome clause that wouldn't stand alone as a complete sentence; rewrite any that describe a feature
4. **Rank by evidence strength** — statements grounded in direct observation rank above those inferred from assumptions
5. **Produce the output** in the format below

---

## Output Format

```
## Needs Statements: [User / Role]
[One sentence on who the user is and what context was researched]

### Needs Statements
1. [User] needs a way to [do X] so that they [benefit].
2. [User] needs a way to [do Y] so that they [benefit].
3. [User] needs a way to [do Z] so that they [benefit].
[3–6 total, ranked by strength of evidence]

### Notes
- [Any statement that was close but reframed, and why]
- [Observations that didn't yield a clear need yet — carry forward to research]
```

---

## Quality checks

Before delivering the output, verify:

- **Every statement has a "so that" clause** — if it reads fine without it, it's a feature, not a need
- **No solution language** — "a dashboard", "a button", "a notification" should not appear in the need; if they do, reframe to the outcome that prompted the solution idea
- **Grounded in evidence** — each statement connects to a specific observation, low, or gap, not a team assumption
- **Specific enough to guide ideation** — "needs a way to manage their work" is too vague; name the specific task or goal
- **User-centred language** — the subject is always the user, never the system or the team

---

## Connecting to other EDT activities

- **edt-empathy-map** — run before Needs Statements when the team doesn't yet have shared observation data; the Empathy Map feeds directly into this activity
- **edt-assumptions-and-questions** — run when writing Needs Statements surfaces things the team is still guessing about rather than knows; those guesses go onto the risk grid
- **Hills** — the natural next step after Needs Statements are agreed; Hills take the strongest needs and reframe them as measurable user outcome goals the team commits to
- **Ideation** — use finalised Needs Statements as the "How might we..." prompts that seed idea generation
