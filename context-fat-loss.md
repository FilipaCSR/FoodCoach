# Context File — Example: Fat Loss Focus

*This is an example of what a filled-in context file looks like for someone focused on fat loss while preserving muscle. It's illustrative — not real data, and not medical advice. Adapt to your own situation.*

---

## Purpose & Context

I'm based in [city] and I'm tracking my meals, macros, and key micronutrients with a focus on losing fat while preserving muscle over the next 12 weeks. Success looks like a 4–6 kg reduction in body weight, with strength maintained on key lifts and energy levels stable through the day.

---

## Current State

### Tracking file

- **Path:** `food_log.csv` in this project
- **Schema:** `Date, Meal, Food, Grams, Protein_g, Carbs_g, Fat_g, Calories`

### Logging approach

- Photos of plated meals, restaurant menus, and packaged labels
- One row per ingredient — combined dishes get decomposed
- Visible label values override estimation
- Cooking fats logged automatically when I cook eggs or vegetables

### Protein staples

- Eggs — boiled or scrambled, ~6.3 g protein per egg
- Chicken breast — grilled, ~31 g protein per 100 g
- Greek yogurt (high-protein) — ~10 g protein per 100 g
- Canned tuna — ~23 g protein per 130 g can
- Whey protein — ~24 g protein per scoop

### Daily targets

- Calories: 1,700–1,900 kcal
- Protein: ≥130 g (≥2 g per kg of target weight)
- Carbs: 130–180 g (higher on training days)
- Fat: 50–70 g

### Micronutrient gaps being addressed

- Iron: borderline — addressing with red meat 2x/week and dark leafy greens daily
- Vitamin D: clear gap — 2,000 IU supplement daily
- Magnesium: monitoring — added pumpkin seeds and almonds as snacks

### Restaurants frequented

[Restaurant 1, Restaurant 2, Restaurant 3]

---

## On the Horizon

- Weekly summary every Sunday (calories, protein average, days hit target, days missed)
- Monthly review of weight trend vs. expected loss rate
- Quarterly review of micronutrient gaps and adjustment

---

## Key Learnings & Principles

- "A small portion" of pasta usually means 60–80 g dry weight for me, not 100 g.
- Skipping breakfast leads to overeating at dinner — keep breakfast even on rest days.
- Late-night eating disrupts sleep — last meal by 8 pm where possible.
- "Healthy" restaurant salads often contain 600+ kcal in dressing and toppings — log them carefully.
- I prefer Greek yogurt brand X over brand Y for the higher protein-to-calorie ratio.

---

## Approach & Patterns

- Meals decomposed into individual ingredients, one row per ingredient.
- Cooking olive oil added automatically when eggs or vegetables are logged.
- Edits use targeted line replacements, not full file rewrites.
- Weekly summary on Sundays unless I ask earlier.
- If protein is below target by Wednesday afternoon, flag it and suggest a high-protein dinner.
