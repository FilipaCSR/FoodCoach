# Food Coach Template

The setup I use to run a personal food coach inside a Claude Project. Three small files and a short setup guide. That's all of it.

## What this is

A Claude Project configuration that turns Claude into a coach that:

- Logs meals from photos into a CSV
- Tracks macros and likely micronutrient coverage
- Suggests swaps when your eating gets repetitive or has gaps
- Gets more personal over time as Claude's memory accrues

The full reasoning is in two posts on Medium:

- **[Why I built my own food coach][post-1-link]** — the perspective behind it
- **[How my food coach actually works][post-2-link]** — the architecture this template comes from

## What's in this repo

```
food-coach-template/
├── README.md                ← you are here
├── project-description.md   ← copy into your Claude Project's description
├── project-instructions.md  ← copy into your Claude Project's instructions
├── food_log.csv             ← starter CSV with the column schema
└── setup-guide.md           ← step-by-step setup
```

## Quick start

1. Create a new Claude Project called "Food Coach" (or whatever you want).
2. Paste `project-description.md` into the project's description field.
3. Paste `project-instructions.md` into the project's instructions field.
4. Add `food_log.csv` as a project file.
5. Make sure Claude's memory feature is on for the project.
6. Start logging — send a photo of a meal, and Claude will estimate, decompose, and append.

That's the whole setup. Most of the personalization happens after you start using it.

## What's *not* in this repo (and why)

You won't find a long context file template with my goals, baselines, and habits to copy. That's not how the system works. Claude's memory builds that up on its own as you log meals, ask questions, and correct things along the way. Trying to pre-fill a "context file" before you start would be writing memory you don't have yet.

The setup is small on purpose. The personalization is yours to grow.

## What this isn't

- **Not an app.** You'll be using this inside Claude, not a custom interface.
- **Not a calorie counter.** The CSV stores macros, but the value is in pattern reading, not arithmetic.
- **Not a replacement for medical advice.** This is a tool for personal experimentation. If you have a medical condition, talk to a doctor, not an LLM.
- **Not finished after setup.** The first week will be rougher than the second. The second rougher than the third. That's expected.

## A note on Claude-specificity

This template is for Claude. The persistent memory feature within Claude Projects is what makes the personalization accrue without you having to engineer it. Other LLMs handle memory differently or not at all — you can adapt the project description and instructions to a long-running ChatGPT conversation or similar, but you'll need to manage memory yourself (paste prior context, keep one long thread, etc.). That's a different system.

## License

MIT. Take it, fork it, change it, share it.

## Credit

Built and maintained by [Filipa Rodrigues][filipa-link]. If you build something with this, I'd love to hear about it!

[post-1-link]: https://medium.com/@filipacsr/why-i-built-my-own-food-coach-972d330beeb4 
[post-2-link]: #
[filipa-link]: https://thehumanruntime.com
