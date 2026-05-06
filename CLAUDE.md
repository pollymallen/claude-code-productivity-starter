# Claude Code Productivity Starter

Open-source starter kit: four markdown templates + five slash commands for file-based personal productivity with Claude Code. MIT licensed.

## Project Structure

```
README.md           ← Public setup guide + walkthrough
TODAY.md            ← Template: daily focus + session notes
WEEK.md             ← Template: weekly priorities, deadlines, promises
BACKLOG.md          ← Template: ideas, someday, waiting-on
PORTFOLIO.md        ← Template: cross-project index
commands/
  start.md          ← /start — daily briefing from files
  wrap.md           ← /wrap — save session state to files
  dump.md           ← /dump — brain dump → auto-sort
  new-project.md    ← /new-project — create a project folder with a plan
  resume-project.md ← /resume-project — pick up a project where you left off
```

## Audience

Blueprint participants and anyone new to Claude Code who wants a simple productivity system before adopting project management tools. The README should stay beginner-friendly — no jargon, no assumed Claude Code knowledge beyond basic install.

## What's In / Out

**In scope:** The four-file system, the five commands, clear setup instructions, "what's next" pointers to more advanced patterns. Per-project PLAN.md and SESSION-LOG.md are created automatically by the commands (not templated).

**Out of scope:** Asana integration, scheduled agents, memory systems. Those are graduation steps mentioned in the README but not built here.

## Writing

Public-facing. Use Polly's brand voice (see `~/.claude/brand-voice.md`). Keep it practical and direct — this is a tool, not a thought piece.
