# Context File — Example: Muscle Gain Focus

*This is an example of what a filled-in context file looks like for someone focused on muscle gain. It's illustrative — not real data, and not medical advice. Adapt to your own situation.*

---

## Purpose & Context

I'm based in [city] and I'm tracking my meals, macros, and recovery markers with a focus on gaining lean muscle over the next 16 weeks. I train resistance 4x/week. Success looks like 2–3 kg of lean mass gained, strength up on key lifts, and waist measurement stable.

---

## Current State

### Tracking file

- **Path:** `food_log.csv` in this project
- **Schema:** `Date, Meal, Food, Grams, Protein_g, Carbs_g, Fat_g, Calories`

### Logging approach

- Photos of plated meals, restaurant menus, and packaged labels
- One row per ingredient — combined dishes get decomposed
- Visible label values override estimation
- Training days are flagged in the Meal column suffix (e.g., "Lunch (training)") to help with post-workout analysis

### Protein staples

- Chicken breast — grilled, ~31 g protein per 100 g
- Lean beef — pan-seared, ~26 g protein per 100 g
- Eggs — scrambled or boiled, ~6.3 g protein per egg
- Cottage cheese — ~11 g protein per 100 g
- Whey protein — ~24 g protein per scoop, used post-workout

### Daily targets

- Calories: 2,600–2,800 kcal (training days), 2,400–2,500 kcal (rest days)
- Protein: ≥160 g (~2 g per kg of body weight)
- Carbs: 280–340 g on training days, 200–240 g on rest days
- Fat: 70–90 g

### Micronutrient gaps being addressed

- Zinc: monitoring — adding pumpkin seeds and oysters when available
- Magnesium: clear gap — 300 mg supplement before bed
- Vitamin D: borderline — 2,000 IU supplement daily

### Restaurants frequented

[Restaurant 1, Restaurant 2, Restaurant 3]

---

## On the Horizon

- Weekly summary every Sunday (protein hit rate, training-day vs rest-day calorie split, sleep average if shared)
- Bi-weekly check on body weight trend (target +0.25 kg/week)
- Monthly review of strength progress vs. nutrition adherence

---

## Key Learnings & Principles

- Post-workout window: aim for 30–40 g protein within 90 minutes of training.
- "Big bowl" of rice means ~200 g cooked for me, not 250 g.
- High-fat meals before training make me sluggish — front-load carbs on training days.
- I prefer cottage cheese brand X for the texture, even though brand Y is cheaper.
- Travel weeks consistently come in low on protein — flag this when I mention travel ahead of time.

---

## Approach & Patterns

- Meals decomposed into individual ingredients, one row per ingredient.
- Training-day suffix added to the Meal column when I mention training that day.
- Cooking olive oil added automatically when eggs or vegetables are logged.
- Edits use targeted line replacements, not full file rewrites.
- Weekly summary on Sundays unless I ask earlier.
- If protein is below target by mid-afternoon on a training day, flag it.
