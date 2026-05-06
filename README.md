# File-Based Task Tracker for Claude Code

A simple productivity system that uses markdown files + Claude Code slash commands. No databases, no apps, no integrations. Just files and an AI that reads them.

## How It Works

Four files track everything:

| File | What it holds | When you touch it |
|------|--------------|-------------------|
| `TODAY.md` | What matters today + session notes | Every session (Claude updates it for you) |
| `WEEK.md` | This week's priorities, deadlines, promises | Weekly (or when things change) |
| `BACKLOG.md` | Ideas, someday items, parked projects | When you brain dump or review |
| `PORTFOLIO.md` | All your projects in one place | When you start or finish a project |

Five commands run the system:

| Command | What it does | When to use it |
|---------|-------------|----------------|
| `/start` | Reads your files, tells you what matters, lets you reprioritize | Beginning of your day |
| `/dump` | You talk, Claude sorts it into the right file | Whenever your brain is full |
| `/new-project` | Creates a project folder with a plan | When you start something new |
| `/resume-project` | Picks up a project where you left off | When you return to a project |
| `/wrap` | Saves session progress to project + daily files | End of a project session |

## Setup (1 minute)

Open Claude Code in the folder where you want to keep your productivity files and paste this:

```
Install the productivity starter kit from https://github.com/pollymallen/claude-code-productivity-starter — fetch the four template files (TODAY.md, WEEK.md, BACKLOG.md, PORTFOLIO.md) into this directory and install the five slash commands (start.md, wrap.md, dump.md, new-project.md, resume-project.md) into ~/.claude/commands/
```

Claude will grab the files from GitHub and put everything in the right place.

Then:

1. **Run `/dump`** and tell Claude everything on your plate. It'll sort it into your files.
2. **Run `/start`** the next morning to see your briefing.

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
   cp commands/*.md ~/.claude/commands/
   ```

3. **Open Claude Code** in your folder and run `/dump` to get started.

</details>

## The Daily Flow

```
/start                  ← Briefing: what matters today, reprioritize if needed
cd project-folder/      ← Move to a project
/new-project or         ← Start something new, or
/resume-project         ← Pick up where you left off
... do work ...         ← Claude helps you with the project
/wrap                   ← Save session progress, update portfolio
```

### `/start` — Morning briefing

`/start` reads all your files and gives you a 3-5 sentence summary: what's the priority, what's due, what's in flight. It also lets you check things off, reprioritize, or add new items before you dive in.

### `/dump` — Brain dump

When your head is full, run `/dump` and talk:

> "I need to finish the proposal by Friday. Also I should email Sarah back about the partnership thing. Oh and I had an idea for a new workshop format — three days instead of one, with homework between sessions. My taxes are due May 15. And I need to buy dog food."

Claude sorts each item into TODAY.md, WEEK.md, or BACKLOG.md based on urgency and type. You don't have to categorize anything yourself.

### `/new-project` and `/resume-project` — Project work

When you have something bigger than a single task, give it a project folder:

- **`/new-project website redesign`** — Claude asks a few questions, creates a project folder with a plan, and adds it to your portfolio
- **`/resume-project`** — Claude reads the plan and session log, tells you where you left off

### `/wrap` — End a project session

When you're done working on a project, `/wrap` saves everything:
- Updates `PLAN.md` — checks off what you finished
- Writes a session entry to `SESSION-LOG.md` — what was done, what's next, any blockers
- Updates `PORTFOLIO.md` — so your cross-project view stays current
- Updates daily/weekly files if anything changed

You can pick up cold next time because everything is in the files.

## What's Next (When You Outgrow This)

This is the zero-to-one. Once you're running smoothly with files:

- **Custom commands** — Build slash commands for your specific workflows (newsletter pipeline, client onboarding, etc.)
- **Scheduled agents** — Set up Claude routines that run on a schedule (daily briefings, weekly reviews)
- **Team tools** — Connect to Asana, Slack, or other systems when you need team visibility

But start here. Files first. Complexity later.
