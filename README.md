# Food Coach Template

A starter kit for building your own food coach with an LLM.

This is the template I use myself. It's not an app — it's a set of files and a method. You bring an LLM (Claude, ChatGPT, or whatever you prefer), the template gives you the structure that makes the LLM useful as a coach instead of a chatbot.

## What this is for

A food coach, in this setup, is an LLM that:

- Knows your goals, your habits, and what you've been eating
- Logs meals from photos in a structured format
- Reads patterns across days, not just single meals
- Answers real questions — "have I been getting enough protein?", "what's the best thing on this menu for me?", "any micronutrient gaps I should close?"
- Gets more personal over time as you correct it

The full reasoning for why I built this — and what the alternatives get wrong — is in two posts on Medium:

- **[Why I built my own food coach][post-1-link]** — the perspective behind it
- **[How my food coach actually works][post-2-link]** — the architecture this template comes from

Read those first if you want the why. Read this README if you want the how.

## What's in this repo

```
food-coach-template/
├── README.md                       ← you are here
├── context-file-template.md        ← the persistent memory the coach reads
├── meal-log-template.csv           ← the log format
├── setup-guide.md                  ← how to get it running
└── examples/
    ├── context-fat-loss.md         ← example context file: fat loss focus
    └── context-muscle-gain.md      ← example context file: muscle gain focus
```

Two files do the real work: `context-file-template.md` and `meal-log-template.csv`. The setup guide tells you how to wire them into an LLM. The examples show what a filled-in context file looks like for different goals.

## Quick start

1. Copy `context-file-template.md` and fill it in with your own goals, habits, and baselines. Don't overthink the first version — it gets better as you use it.
2. Copy `meal-log-template.csv` to wherever you want the log to live (a local file, Google Drive, a project folder).
3. Follow `setup-guide.md` to set up the coach in your LLM of choice.
4. Start logging. Correct the coach when it gets things wrong. Move corrections back into the context file.

That's the whole loop.

## What this isn't

- **Not an app.** You'll be using this inside an LLM chat, not a custom interface.
- **Not a calorie counter.** The CSV stores macros, but the coach's value is in pattern reading, not arithmetic.
- **Not a replacement for medical advice.** This is a tool for personal experimentation. If you have a medical condition, talk to a doctor, not an LLM.
- **Not finished.** The first version of your context file will be rougher than the version six months in. The point is to start, not to start perfect.

## License

MIT. Take it, fork it, change it, share it.

## Credit

Built and maintained by [Filipa Castro][filipa-link]. If you build something with this, I'd love to hear about it.

[post-1-link]: #
[post-2-link]: #
[filipa-link]: https://thehumanruntime.com
