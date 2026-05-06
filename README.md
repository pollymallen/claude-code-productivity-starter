# File-Based Task Tracker for Claude Code

A simple productivity system that uses markdown files + Claude Code slash commands. No databases, no apps, no integrations. Just files and an AI that reads them.

## How It Works

Three files track everything:

| File | What it holds | When you touch it |
|------|--------------|-------------------|
| `TODAY.md` | What matters today + session notes | Every session (Claude updates it for you) |
| `WEEK.md` | This week's priorities, deadlines, promises | Weekly (or when things change) |
| `BACKLOG.md` | Ideas, someday items, parked projects | When you brain dump or review |

Three commands run the system:

| Command | What it does | When to use it |
|---------|-------------|----------------|
| `/start` | Reads your files, tells you what matters | Beginning of every session |
| `/wrap` | Saves everything from the session to files | End of every session |
| `/dump` | You talk, Claude sorts it into the right file | Whenever your brain is full |

## Setup (1 minute)

Open Claude Code in the folder where you want to keep your productivity files and paste this:

```
Install the productivity starter kit from https://github.com/pollymallen/claude-code-productivity-starter — fetch the three template files (TODAY.md, WEEK.md, BACKLOG.md) into this directory and install the three slash commands (start.md, wrap.md, dump.md) into ~/.claude/commands/
```

Claude will grab the files from GitHub and put everything in the right place.

Then:

1. **Run `/dump`** and tell Claude everything on your plate. It'll sort it into the three files.
2. **Run `/start`** at the beginning of each session. Run `/wrap` at the end.

That's it. The system builds itself from your first brain dump.

<details>
<summary>Manual setup (if you prefer)</summary>

1. **Clone this repo** into wherever you keep projects:
   ```
   git clone https://github.com/pollymallen/claude-code-productivity-starter.git ~/my-system
   cd ~/my-system
   ```

2. **Install the slash commands.** Claude Code looks for custom commands in `~/.claude/commands/`. Create that folder if it doesn't exist, then copy the commands in:
   ```
   mkdir -p ~/.claude/commands
   cp commands/start.md ~/.claude/commands/
   cp commands/wrap.md ~/.claude/commands/
   cp commands/dump.md ~/.claude/commands/
   ```

3. **Open Claude Code** in your folder and run `/dump` to get started.

</details>

## The Daily Loop

```
/start          ← Claude reads your files, gives you a briefing
... do work ... ← Claude helps you with tasks
/wrap           ← Claude saves session notes + updates your files
```

## The Brain Dump

When your head is full, just run `/dump` and talk:

> "I need to finish the proposal by Friday. Also I should email Sarah back about the partnership thing. Oh and I had an idea for a new workshop format — three days instead of one, with homework between sessions. My taxes are due May 15. And I need to buy dog food."

Claude will sort each item into TODAY.md, WEEK.md, or BACKLOG.md based on urgency and type. You don't have to categorize anything yourself.

## What's Next (When You Outgrow This)

This is the zero-to-one. Once you're running smoothly with files:

- **Project folders** — Give each project its own folder with a `PLAN.md` and `SESSION-LOG.md`
- **Asana integration** — Connect your task tracker to Asana for team visibility
- **Custom commands** — Build slash commands for your specific workflows (newsletter pipeline, client onboarding, etc.)
- **Scheduled agents** — Set up Claude routines that run on a schedule (daily briefings, weekly reviews)

But start here. Files first. Complexity later.
