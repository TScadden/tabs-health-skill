# Tabs Health Q&A — Agent Skill for Google AI Edge Gallery

A private, on-device health companion skill. Ask about your Tabs health data
(recent logs, sleep, heart rate, trends) and the Gemma model answers from your
own server's data. Nothing is sent to a cloud AI; the only network call is the
encrypted fetch to your own Tabs server (`api.jottracker.com`).

## Load it in the Gallery app

1. Open **Google AI Edge Gallery** on your Android phone.
2. Go to **Agent Skills → + → Load from URL**.
3. Paste:
   ```
   https://tscadden.github.io/tabs-health-skill/tabs-health-qa/SKILL.md
   ```
4. When prompted for the secret, enter your Tabs login as `email:password`.
   The skill logs in, pulls your data, and closes the session immediately.
   Change your Tabs password any time to revoke it.

## Files

```
tabs-health-qa/
├── SKILL.md            # Skill definition: instructions the on-device model follows
└── scripts/
    └── index.html      # JavaScript engine: login → pull → trim → logout
```

## What it can answer

- "How did I sleep this week?"
- "Any heart rate spikes lately?"
- "What have I logged the past few days?"
- "Summarize my recent insights."

Read-only by design: it cannot log, edit, or delete anything, and it never
suggests changing hydration, medication, or supplements.
