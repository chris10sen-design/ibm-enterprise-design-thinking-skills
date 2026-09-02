---
name: edt-assumptions-and-questions
description: >-
  Run an IBM Enterprise Design Thinking Assumptions and Questions activity to surface what the team believes
  to be true and what they still don't know, then prioritise which uncertainties pose the highest risk.
  Two modes - Facilitate (agent guides a live session) or Synthesize (agent organises existing sticky note
  output and builds an action plan). Use whenever the team needs a reality check, wants to surface hidden
  risks, or is about to make decisions based on untested beliefs. Trigger phrases include "assumptions and
  questions", "reality check", "what are we assuming", "surface our unknowns", "risk check", "what don't
  we know", "validate our assumptions", "assumptions mapping", "identify risks", "what assumptions are we
  making", "high risk assumptions", "what questions do we still have", "what could go wrong", "are we sure
  about this", "test our assumptions", "what are we guessing", "risk mapping", "unknown unknowns".
metadata:
  display_name: EDT Assumptions & Questions
  short_description: Surface and prioritise team assumptions and open questions using the EDT risk grid
  author: Jan Christensen
  version: "0.1"
---

# Assumptions and Questions

Assumptions and Questions is a team activity that brings honesty into a project. Every team is operating
on a mix of things they know, things they assume are true, and things they haven't figured out yet. This
activity makes that invisible mix visible — so the team can focus their energy on reducing the risks that
matter most.

**When to use it:**
- Early in a project, before decisions harden around untested beliefs
- Before a major milestone when you want a "reality check"
- When the team feels like it's moving fast but isn't sure it's moving in the right direction
- After research — to separate confirmed knowledge from lingering guesses
- As often as needed — risk never disappears, but it can be managed

**Time:** 30 minutes (can expand to 90 for complex projects)

**Core principle:** An unasked question will forever go unanswered. Don't hold back even if a question
seems naive — the riskiest assumptions are often the ones nobody wanted to name.

---

## Step 0 — Choose your mode

Before starting, ask:

> *"Are you running this activity with your team right now — I'll help you surface and place your assumptions and questions — or do you already have output from a session you want me to help organise and act on?"*

- **Facilitate mode** → agent prompts the user to surface assumptions and questions, places them on the grid, identifies the highest-risk items, and builds an action plan
- **Synthesize mode** → user pastes or describes existing output; agent organises items onto the grid, identifies the upper-right quadrant, and builds the action plan

---

## Facilitate Mode

Work through each phase in order. The critical discipline is: **write before you talk**. Get items on paper individually before any discussion — this prevents the loudest voice from collapsing everyone else's honest uncertainty.

### Phase 1 — Set up the grid

Explain the activity:

> *"We're going to map everything your team currently believes — and everything you're not sure about — onto a 2×2 grid:*
>
> *- **Top** = High-risk (if we're wrong, it seriously affects the project)*
> *- **Bottom** = Low-risk (being wrong wouldn't change much)*
> *- **Left** = Certain (we have evidence or strong confidence)*
> *- **Right** = Uncertain (we're guessing, haven't checked, or genuinely don't know)*
>
> *The upper-right corner — high-risk and uncertain — is where we need to focus."*

### Phase 2 — Collect assumptions and questions

Ask the user to generate items *individually* before any filtering or discussion. Push for volume first.

> *"Write down every assumption your team is making and every question that still doesn't have a clear answer. One per sticky note. Don't filter yet — include the ones that feel obvious, the ones that feel embarrassing, and the ones you've been avoiding.*
>
> *Prompts to get started:*
> *- What are we assuming is true about our users?*
> *- What are we assuming about the market or the problem?*
> *- What are we assuming about our own ability to deliver?*
> *- What questions do we keep deferring?*
> *- What would we need to know to be fully confident in our direction?*
> *- What would make us change course if we found out it was wrong?"*

Wait for the user to share their list. Don't start evaluating yet.

### Phase 3 — Place items on the grid

Work through each item together. For each one, ask two questions:

1. *"How risky is this — if you found out you were wrong about this, would it significantly change what you're building or how?"* (High / Low)
2. *"How certain are you right now — do you have real evidence for this, or are you guessing?"* (Certain / Uncertain)

Place each item in the appropriate quadrant. Keep this quick — individual placement first, then reposition as a group when patterns become clear.

### Phase 4 — Identify the upper-right quadrant

Once all items are placed, focus on the **upper-right: high-risk + uncertain**.

> *"These are the items that could derail the project if you're wrong, and you don't have strong evidence for them yet. These are your priority risks."*

Name and list them clearly. If there are more than 5–7, help the user narrow to the most critical ones.

### Phase 5 — Build an action plan

Pull the high-risk + uncertain items into a separate list. For each one, diverge on how to validate or invalidate it. The question to ask for each item:

> *"What's the fastest, cheapest way to find out if this is true or false?"*

Common validation approaches:
- **Talk to someone directly** — a user, a subject-matter expert, a colleague who has done this before
- **Direct observation** — watch a user in context, look at existing data or logs
- **Prototype and test** — build the smallest possible thing that tests the assumption
- **Desk research** — find existing studies, reports, or data that answer the question
- **Survey or poll** — get quick signal from a larger group

For each high-risk uncertain item, produce one action:

```
Assumption / Question: [item]
Validation approach: [what you'll do]
Who will do it: [person or role]
How you'll know: [what evidence would confirm or deny this]
```

### Phase 6 — Playback

Produce the completed grid and action plan as a structured artifact (see Output Format below) and offer:

> *"Would you like to move into an Empathy Map to ground some of these user assumptions in real observation data? Or if you've already done user research, a Research Synthesis session could help you work through what you already know."*

---

## Synthesize Mode

Ask the user to share their output:

> *"Paste in your sticky note content, notes from the session, or describe what came out of the activity. Include everything — I'll organise it onto the grid."*

Once you have the input:

1. **Classify each item** as an assumption (something believed to be true) or a question (something unknown)
2. **Place on the grid** — assess risk level (high/low) and certainty level (certain/uncertain) for each item
3. **Identify the upper-right cluster** — high-risk + uncertain items are the action priority
4. **Build the action plan** — for each upper-right item, propose a validation approach using the approaches in Phase 5 of Facilitate Mode (talk to someone, observe directly, prototype and test, desk research, survey). Format each action as: assumption/question, validation approach, who will do it, how you'll know.
5. **Produce the artifact** in the output format below

---

## Output Format

```
## Assumptions and Questions: [Project / Product / Feature name]
Date: [if provided]

### High-risk + Uncertain (act on these first)
| # | Item | Type | Validation approach |
|---|------|------|---------------------|
| 1 | [assumption or question] | Assumption / Question | [how to validate] |
| 2 | [...] | | |

### High-risk + Certain (monitor these)
- [item] — [brief note on what makes us confident]

### Low-risk + Uncertain (keep an eye on these)
- [item]

### Low-risk + Certain (safe ground)
- [item]

### Action plan
For each item in the upper-right quadrant:

**[Item]**
- Validation approach: [...]
- Who: [person or role]
- How we'll know: [evidence that confirms or denies]

### Items to carry forward
- Assumptions that need an Empathy Map or user research to validate: [list]
- Questions that need a Research Plan to answer: [list]
```

---

## Facilitation principles

- **Do this early and often.** The sooner risk is visible, the sooner it can be reduced. Don't save this for a mid-project "reality check."
- **Write before you talk.** Individual placement before group discussion. This matters — group discussion before placement collapses honest uncertainty into false consensus.
- **Don't hold back.** The most dangerous assumptions are the ones nobody wanted to name. Naive-sounding questions are often the most important ones.
- **Assumptions aren't inherently bad.** Every project runs on assumptions. The goal isn't to eliminate them — it's to know which ones are high-risk and act on those.
- **Reposition as a group.** After individual placement, compare and discuss. Items often move when the team sees how differently people assessed the same thing.

---

## Common mistakes to avoid

| Mistake | Why it matters | Fix |
|---|---|---|
| Only listing questions, not assumptions | Assumptions are often riskier because they feel settled | Explicitly prompt for "what are we assuming is true?" |
| Treating all uncertainty as equal | Not everything uncertain matters equally | Force the risk dimension — would being wrong change what you build? |
| Building a list with no action plan | The grid is useless without follow-through | Every upper-right item needs a specific validation action |
| Doing this once and never returning | New work generates new assumptions constantly | Schedule this activity at major milestones or decision points |
| Vague items like "users will like it" | Too broad to validate | Push to: "Users will find the onboarding flow easy enough to complete without help" |

---

## Connecting to other EDT activities

- **edt-empathy-map** — run first when user-related assumptions are plentiful and the team doesn't yet have shared observation data; the map grounds guesses in real evidence
- **edt-research-synthesis** — run when existing interview or field research can already answer some of the upper-right questions; skip to synthesis rather than doing new research
- **edt-needs-statements** — run after synthesis when user-related assumptions reveal you don't yet know what the user actually needs
- **Research Plan** — convert high-risk uncertain questions that can't be resolved internally into a structured study with clear objectives
- **Hills** — run after Assumptions and Questions when upper-right items reveal the team lacks clear user outcome goals; Hills force that clarity before more work is done
