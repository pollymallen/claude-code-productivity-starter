# /new-project — Start a New Project

Start a new project: $ARGUMENTS

## Steps

### 1. Quick Context

Ask the user 3-5 questions to understand the project:
- What's the goal?
- Who's it for?
- Any deadline or constraints?
- What does "done" look like?

Keep it conversational — don't interrogate.

### 2. Create the Project Folder

Create a folder for the project in the current directory. Use a short, lowercase, hyphenated name (e.g., `website-redesign/`).

### 3. Enter Plan Mode

Use Claude Code's built-in plan mode to create a `PLAN.md` in the new project folder. The plan should include:
- Project name and one-line summary
- Goals with checkboxes
- Phases or task breakdown
- Success criteria
- Any risks or blockers

Claude Code will create the `PLAN.md` automatically when you plan.

### 4. Add to PORTFOLIO.md

Add a line to the **Active** section of `PORTFOLIO.md` (in the root of your system folder):

```
- **[Project Name]** (`folder/`) — Status: In Progress, Next: [first task]
```

### 5. Confirm

Show the user:
- The project folder and plan
- Where it appears in the portfolio
- What the first task is

Ask: "Ready to start working, or want to adjust the plan?"

---

## When the Session Ends

When the user wraps up:
1. Update `PLAN.md` — check off completed tasks, update status
2. Add a session entry to `SESSION-LOG.md` in the project folder (create it if it doesn't exist) with: date, what was done, what's next, any blockers
3. Update `PORTFOLIO.md` if the project status changed
