---
name: edt-empathy-map
description: >-
  Run an IBM Enterprise Design Thinking Empathy Map to build shared team understanding of a user by mapping
  what they Say, Do, Think, and Feel. Two modes - Facilitate (agent guides a live session quadrant by
  quadrant) or Synthesize (agent structures, clusters, and surfaces patterns from existing session output).
  Use whenever the team needs to align on who they are designing for, is losing focus on the user, or has
  just come out of interviews and needs to structure what they heard. Trigger whenever someone mentions
  "empathy map", "understand our users", "map user perspective", "what does our user think and feel",
  "run an empathy map", "build user empathy", "understand user motivations", "map what users say and do",
  "who is our user", "user perspective", "user research debrief", "after the interviews", "what do users
  care about", "user attitudes", "user behaviour", "design thinking session", "voice of the customer",
  "what are users experiencing", "user needs and emotions".
metadata:
  display_name: EDT Empathy Map
  short_description: Build shared user understanding by mapping what users Say, Do, Think, and Feel
  author: Jan Christensen
  version: "0.1"
---

# Empathy Map

An Empathy Map is a collaborative activity that puts your team in your users' shoes. It creates a shared
picture of what a user Says, Does, Thinks, and Feels — drawing on everyone's observations and knowledge
rather than any one person's assumptions.

**When to use it:**
- Before an important design or product decision
- Directly after an observation or interview session
- When the team has lost focus on the user and needs to re-center
- At the start of a project to align on who you're designing for

**Time:** 30 minutes (can expand to 60 for deeper sessions)

**Core reminder:** You are not your user. The map is only as good as the real observations behind it.

---

## Step 0 — Choose your mode

Before starting, ask:

> *"Are you running this activity with your team right now — meaning you'll answer the questions as you go — or do you already have sticky notes, notes, or output from a session you want me to help structure?"*

- **Facilitate mode** → agent asks the questions; the user (or the user proxying for their team) answers; agent builds the map from those answers
- **Synthesize mode** → user pastes or describes existing output; agent clusters, identifies patterns, and produces the final map

---

## Facilitate Mode

Work through each phase in order. Don't rush — the value is in the diverge step where everyone writes before anyone talks.

### Phase 1 — Set up the map

Tell the user:

> *"We're going to map your user across four quadrants: **Says** (things they say out loud), **Does** (actions and behaviours), **Thinks** (internal thoughts they might not say aloud), and **Feels** (emotional states and reactions).*
>
> *First: who is the user we're mapping? Give them a name and a one-sentence description of who they are and what they do."*

Wait for the user to name and describe the user. Confirm before continuing.

### Phase 2 — Capture observations

Work through each quadrant one at a time. For each quadrant, ask the prompt, then wait for the user to respond before moving on. Encourage multiple responses — aim for at least 3–5 per quadrant.

**Says:**
> *"What does [user name] actually say — in their own words — about this experience? What phrases or quotes have you heard? What do they complain about, ask for, or express?"*

**Does:**
> *"What does [user name] do — what actions do they take, what behaviours have you observed? What workarounds do they use? What do they do when things go wrong?"*

**Thinks:**
> *"What might [user name] be thinking but not saying aloud? What concerns, doubts, or internal reactions do you think they have? What do they worry about?"*

**Feels:**
> *"How does [user name] feel during this experience — what emotions come up? Where are the moments of frustration, anxiety, confusion, or relief?"*

After all four quadrants are filled, prompt:

> *"Are there any observations you're not sure about — things that feel like assumptions rather than things you've actually seen or heard? Let's flag those — they'll be useful for Assumptions and Questions later."*

### Phase 3 — Cluster and find patterns

Review all the inputs together. Look for:
- **Cross-quadrant connections** — a behaviour in Does that matches an emotion in Feels, or something in Says that contradicts something in Does; these tensions are often the most useful design signals
- **Contradictions** — when what a user says differs from what they do, that gap is almost always worth exploring
- **Gaps** — quadrants with sparse or no content are not empty sections; they signal areas where the team has been guessing rather than observing
- **Recurring themes** — observations that appear in multiple quadrants or were mentioned by multiple people carry stronger signal than one-offs
- **Emotional intensity** — strong negative feelings (frustration, anxiety, confusion) identify friction points; strong positive ones identify what to preserve

Group related observations into 2–4 named themes. Name them in plain language that describes the user's experience, not the product's feature (e.g., "confusion about next steps" not "navigation problem").

Summarise the patterns in plain language:
> *"Here's what the map is telling us: [summary of 2–4 themes]. The areas where we have the least certainty are [gaps — these feed Assumptions and Questions]. The strongest signal is [top 1–2 findings]."*

### Phase 4 — Playback

Produce the completed map as a structured artifact (see Output Format below) and offer:

> *"This is ready to share with stakeholders or Sponsor Users to validate. Would you like to also surface the flagged assumptions as an Assumptions and Questions activity?"*

---

## Synthesize Mode

Ask the user to share their output:

> *"Paste in your sticky note content, notes from the session, or describe what came out of the activity. Include anything — messy is fine. Organise it however makes sense to you: by quadrant, by observation, or just as a dump."*

Once you have the input:

1. **Sort** every observation into the four quadrants (Says / Does / Thinks / Feels). If something doesn't clearly fit one quadrant, use your best judgement and flag it.
2. **Cluster** items within each quadrant into 2–4 themes. Name each cluster in plain language from the user's perspective.
3. **Identify** the strongest patterns — observations that appear across multiple quadrants, strong emotional signals, contradictions, and gaps (quadrants with sparse content).
4. **Flag assumptions** — observations that read like team beliefs rather than things actually witnessed. Collect these separately and explicitly name them as candidates for an edt-assumptions-and-questions session — this is where many teams find their highest-risk unknowns.
5. **Identify contradictions** — items where Says conflicts with Does. Name the contradiction explicitly; it is a design opportunity, not a data error.
6. **Produce the completed map** in the output format below.

---

## Output Format

Produce the Empathy Map as a clean markdown document:

```
## Empathy Map: [User Name / Role]
[One sentence description of who this user is]

### Says
- [Direct quote or paraphrase of something they've said]
- [...]

### Does
- [Observed action or behaviour]
- [...]

### Thinks
- [Inferred internal thought or concern]
- [...]

### Feels
- [Emotional state observed or inferred]
- [...]

### Key patterns
- [Pattern 1 — cross-quadrant connection or recurring theme]
- [Pattern 2]

### Gaps and assumptions to validate
- [Observation that felt uncertain or assumed rather than witnessed]
- [Quadrant with very little content — signal of unknown territory]

### Recommended next step
[One of: edt-assumptions-and-questions (if many unknowns surfaced) | edt-needs-statements (if patterns are clear enough to frame user needs) | edt-research-synthesis (if the team needs to map the full workflow before narrowing to needs)]
```

---

## Facilitation principles (for any mode)

These come from the official EDT toolkit deck and apply whether the agent is facilitating or synthesizing:

- **Write before you talk.** Individual observation before group discussion prevents groupthink.
- **You are not your user.** The map should reflect observed behaviour and real quotes — not what the team assumes or hopes.
- **Involve Sponsor Users when you can.** Share the map with real users to validate or invalidate observations.
- **Go beyond job title.** Focus on actual tasks, motivations, goals, and obstacles — not role descriptions.
- **Contradictions are useful.** If what a user *says* conflicts with what they *do*, that tension is a design opportunity.
- **Gaps are useful too.** Sparse quadrants reveal where the team has been guessing rather than observing.

---

## Common mistakes to avoid

| Mistake | Why it matters | Fix |
|---|---|---|
| Writing features in the quadrants | The map is about the user's experience, not the product | Redirect any "they need a dashboard" to "they feel overwhelmed trying to track X" |
| Only one person filling the map | The value is in diverse perspectives — solo maps are thin | Ask what other team members would add; flag what you're not sure about |
| Using job titles instead of people | "The admin" is not a person | Give the user a name, a context, a specific workflow |
| Conflating Says and Thinks | Says = things actually spoken; Thinks = internal, unspoken | Keep them separate — the gap between them is often the most interesting finding |
| Skipping the gaps | Teams rush to patterns and miss the blank spaces | Explicitly ask "what quadrant has the least real evidence?" |

---

## Connecting to other EDT activities

- **edt-assumptions-and-questions** — run this immediately when many observations in the map are flagged as assumed rather than witnessed; the map's gaps become the upper-right quadrant candidates
- **edt-research-synthesis** — run this when the Empathy Map patterns are strong enough to move into building an As-Is Scenario Map; Research Synthesis takes over from here
- **edt-needs-statements** — run directly after the map when patterns are clear enough to frame what the user actually needs, without needing a full scenario map first
- **Research Plan** — use the gaps and flagged assumptions as the research objectives for a focused follow-up study with real users
