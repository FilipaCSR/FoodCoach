# Setup Guide

This walks you through getting the food coach running. The instructions are written for Claude (Projects feature), but the same pattern works in any LLM that supports persistent context.

## Step 1: Fill in the context file

Open `context-file-template.md` and replace the placeholders with your own information. Some sections will be detailed from day one (Purpose & Context, Current State); others will be sparse and grow over time (Key Learnings & Principles).

Don't try to predict everything. The Approach & Patterns section, in particular, fills in as you correct the coach. A bare first version is fine.

## Step 2: Set up the log

Copy `meal-log-template.csv` to wherever you want it to live. Options:

- **Local file** — simplest, but only accessible from one device
- **Cloud storage** (Google Drive, Dropbox) — accessible everywhere
- **Project folder in your LLM** — most LLMs let you attach files to a project so they're available in every conversation

I use a CSV in a project folder. Whatever you pick, make sure the path is reachable from wherever you'll be having coach conversations.

## Step 3: Wire it into your LLM

The goal is for the coach to have access to two things in every conversation: the context file and the log.

### If you're using Claude Projects

1. Create a new project called "Food Coach" (or whatever you want).
2. Add `context-file-template.md` (filled in) as a project file.
3. Add your meal log CSV as a project file.
4. In the project's custom instructions, paste the seed prompt below.

### If you're using ChatGPT or another LLM

1. Use a long-running conversation, or set up a custom GPT / equivalent feature.
2. Paste the filled-in context file at the start of each session, or attach it as a file.
3. Attach the CSV as a file (or paste recent rows if your LLM doesn't support file attachments).
4. Use the seed prompt below as the system prompt or first message.

### Seed prompt

```
You are my food coach. I've shared a context file (context.md) with my goals,
habits, baselines, and conventions, and a meal log (food_log.csv) with my
recent meals.

Your job:
- Help me log meals from photos. When I share a photo of a meal, menu, or
  packaged label, decompose it into individual ingredients and append rows
  to the CSV. One row per ingredient. Visible label values override estimation.
- Apply the defaults from the context file without being prompted (cooking
  fats, recurring staples, etc.).
- Answer questions about how I've been eating across days, not just single
  meals — protein adequacy, micronutrient gaps, alignment with my goals.
- When I'm at a restaurant and share a menu, suggest the best option for me
  given what I've been eating recently and what I'm working toward.
- When I correct you, update the context file — not just the moment.

Read the context file before answering any question.
```

You can adapt this. The important parts are: read the context file, decompose meals, apply defaults, answer across days, update the file when corrected.

## Step 4: Start logging

Begin with whatever feels natural. A photo of breakfast, a question about lunch, a menu from dinner. The coach will be rough at first — that's expected.

When it gets something wrong, two things should happen:

1. Fix the immediate thing (re-log the meal, change the row, clarify the question).
2. Move the correction back into the context file. If a phrase was ambiguous, that goes in *Key Learnings & Principles*. If a default was missing, that goes in *Current State* or *Approach & Patterns*. If a goal was misunderstood, that goes in *Purpose & Context*.

This is the loop that makes the system more personal over time. Without it, the coach stays generic.

## Step 5: Iterate

After a week, look at the context file again. Is anything in it stale? Anything missing that came up repeatedly in conversation? Update it.

After a month, the file should look meaningfully different from the version you started with. That's the system working as intended.

## Common questions

**How long should the context file be?**

Mine sits between half a page and a page when I trim it. Longer than that and it starts taking up tokens better spent on actual reasoning. If a section grows beyond what feels useful, prune the bullets that are no longer relevant.

**Do I need to start each conversation fresh?**

Depends on the LLM. In Claude Projects, the context file is available in every conversation automatically — you can start fresh each time and not lose continuity. In other setups, you may want to keep one long conversation, or paste the context file at the start of each new one.

**What if I don't want to track macros?**

Change the CSV columns to whatever you actually care about — sodium, fiber, specific micronutrients, glycemic load, satiety scores. The template uses macros because that's what I track; the structure works with any columns.

**What if the coach hallucinates a number?**

For exact nutrient values where the number really matters (specific micronutrient amounts, supplement doses), verify against a database. The coach is for judgment and pattern reading. Look-up tables are for facts.

**Can I share my context file with someone else?**

The whole point of the context file is that it's about *you*. Sharing it doesn't help anyone else, and the structure is what matters anyway — that's already in this template. Share the template, not your file.
