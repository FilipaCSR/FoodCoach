# Setup Guide

This is the actual setup behind the food coach in [the Medium posts][post-1-link]. Five steps. Should take about five minutes.

## 1. Create a Claude Project

In Claude, create a new Project. You can call it "Food Coach" or whatever fits.

If you're new to Projects: a Project is a workspace where Claude has access to specific files and instructions across every conversation you have inside it. It's how the coach stays consistent across sessions instead of starting from zero each time.

## 2. Set the project description

Open `project-description.md`, copy the description text, and paste it into your project's description field.

The description is short on purpose. It tells Claude what the project is *for*. The behavior comes from the next step.

## 3. Set the project instructions

Open `project-instructions.md`, copy the instruction text, and paste it into your project's instructions field.

This is the most important file in the repo. It defines what Claude does when you upload a meal photo, what micronutrients to track, when to summarize. Adapt it freely:

- **Different micronutrients** — change the list to whatever you care about.
- **Different summary cadence** — weekly is mine; daily, biweekly, or monthly all work.
- **Different log fields** — if you want to track sodium, fiber, glycemic load, or anything else, add it to the instruction.
- **Different goals** — if you're focused on a specific outcome (fat loss, muscle gain, energy, recovery), say so. The coach will adapt suggestions to that focus.

## 4. Add the CSV

Add `food_log.csv` to the project as a file. It starts empty (just the column headers). Claude will append rows to it as you log meals.

If you'd rather use different columns, edit the CSV before you add it. Whatever columns are in the file are what Claude will use.

## 5. Make sure memory is on

Claude's memory feature needs to be enabled for the personalization to accrue over time. This is what lets the coach remember your habits, your preferences, the corrections you've made, the patterns you're investigating — without you having to re-tell it each session.

You can check the memory setting in Claude's settings (look for "Memory" or "Personalization"). It should be on at the account level, and on for this project specifically if there's a per-project toggle.

## How it grows

The setup above is small on purpose. Most of what makes the coach actually useful — knowing your protein staples, your favorite restaurants, the foods you eat repeatedly, the corrections you've made — *isn't* configured. It accrues.

Day one, the coach is generic. By week two, it knows you cook eggs in olive oil and stops asking. By month two, it knows what "the usual" means at your favorite lunch spot. By month six, it's caught patterns you didn't know were there.

That's the system working. The setup is just the seed.

## What you can do to help it along

Three small habits that make the personalization land faster:

1. **Correct things immediately.** If Claude estimates a portion wrong, say so. If it interprets a phrase the way you didn't mean it, clarify. The corrections become memory.

2. **Use natural language about your goals and habits.** Don't try to "configure" Claude — just talk. "I'm trying to gain muscle this month" or "I always cook with cast iron" lands in memory the same way explicit instructions would.

3. **Ask real questions.** Don't just log. Ask "have I been getting enough protein this week?" or "what's the best thing on this menu for me?" The coach gets sharper through use.

## Common questions

**What if I don't want to track macros?**

Change the CSV columns to whatever you actually care about — sodium, fiber, specific micronutrients, glycemic load, satiety. The structure works with any columns. Update the project instructions to match.

**Do I need to start each conversation fresh, or keep one long thread?**

Either works. With memory on, fresh conversations carry the personalization automatically. 

**What if Claude hallucinates a number?**

For exact nutrient values that really matter (specific micronutrient amounts, supplement doses), verify against a database. The coach is for judgment and pattern reading. Look-up tables are for facts.


[post-1-link]: https://medium.com/@filipacsr/why-i-built-my-own-food-coach-972d330beeb4 
