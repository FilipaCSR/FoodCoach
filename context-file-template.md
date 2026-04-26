# Context File

This is the persistent memory the food coach reads at the start of each conversation. Fill in the placeholders with your own information. Don't worry about getting it perfect — most sections are designed to be updated over time.

The file has five sections, each with a different update cadence. Keep that structure: it's the part that makes the system maintainable instead of a chore.

---

## Purpose & Context

*Update frequency: rarely (only when goals shift)*

[Where you're based, what you're tracking, your primary goal, what success looks like. 2–4 sentences.]

**Example shape:**

> I'm based in [location] and I'm tracking [what you track — meals, macros, micronutrients, etc.] with a focus on [primary focus — fat loss, muscle gain, mental performance, general health, etc.]. Success looks like [specific success criteria — a number, a feeling, a milestone, a window of time].

---

## Current State

*Update frequency: monthly or as patterns shift*

The active stuff. This is where most of the system's day-to-day intelligence lives.

### Tracking file

- **Path:** [where your CSV lives — local path, cloud link, project folder]
- **Schema:** `Date, Meal, Food, Grams, Protein_g, Carbs_g, Fat_g, Calories` (or whatever columns you decide on)

### Logging approach

[How meals get captured. Examples:]

- Photos of plated meals, restaurant menus, and packaged labels
- Each ingredient on its own row — combined dishes get decomposed
- Visible label values override estimation
- [Add your own conventions as you develop them]

### Protein staples

[Frequently-eaten high-protein foods with relevant details. Format: food — preparation note — grams of protein per typical serving.]

- [Food 1] — [preparation note], [protein g per serving]
- [Food 2] — [preparation note], [protein g per serving]
- [Food 3] — [preparation note], [protein g per serving]

### Micronutrient gaps being addressed

[Which nutrients are clearest gaps, which are borderline, what you've added to address them.]

- [Nutrient 1]: [gap status — clear gap / borderline / monitoring], addressing with [foods or supplement]
- [Nutrient 2]: [gap status], addressing with [foods or supplement]

### Physical patterns being investigated

[Symptoms or patterns you've noticed, your current hypothesis, what you'd do if it persists.]

- [Symptom or pattern] — likely linked to [hypothesis]; [recommended next step] if it persists

### Restaurants frequented

[Comma-separated list. Helps the coach when you ask about menus.]

[Restaurant 1, Restaurant 2, Restaurant 3]

---

## On the Horizon

*Update frequency: quarterly*

[Recurring tasks the coach should expect. 2–3 bullets.]

- [Recurring task 1 — e.g., weekly summary every Sunday]
- [Recurring task 2 — e.g., monthly check on protein average]
- [Recurring task 3 — e.g., quarterly review of micronutrient gaps]

---

## Key Learnings & Principles

*Update frequency: monthly — new entries added as new clarifications happen*

[Specific facts the coach should remember to avoid re-litigating. Ambiguous phrasing you've clarified, attributions for past symptoms, product preferences with reasons. One principle per bullet.]

- [Phrase] is ambiguous — it may mean [A] or [B]; confirm with [resolution method].
- [Past symptom] was attributed to [cause]; [resolution].
- I prefer [Product A] over [Product B] for [specific use case] because [reason].
- [Environmental or contextual note — e.g., I cook with cast iron, I don't eat after 8pm, etc.]

---

## Approach & Patterns

*Update frequency: rarely*

[How you and the coach work together day-to-day. The standard editing pattern, how items should be broken out, when summaries are generated. 4–6 bullets.]

- Meals are decomposed into individual ingredients, one row per ingredient.
- Cooking fats are logged automatically when [specific meals are made] without being prompted.
- Edits use targeted line replacements, not full file rewrites.
- Weekly summaries are produced on request or when enough days have accumulated.
- [Add your own patterns as you develop them]
