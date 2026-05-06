# /resume-project — Pick Up Where You Left Off

Resume work on a project.

## Steps

### 1. Find the Project

**If you're already in a project folder** (it has a `PLAN.md`):
- This is the project — proceed to step 2

**If you're in the system root** (where PORTFOLIO.md lives):
- Read `PORTFOLIO.md`
- Show the list of active projects
- Ask: "Which project do you want to work on?"
- Navigate to that project's folder

**If no project files or portfolio exist:**
- Tell the user: "No project found. Run `/new-project [name]` to start one."

### 2. Read Project Files

Read these files from the project folder:
- `PLAN.md` — the plan of record (goals, tasks, phases)
- `SESSION-LOG.md` — start with the **Project Context** block at the top for the full arc, then read the most recent session entries for specifics

### 3. Summarize

Present a brief status update:

```
## Project: [Name]

**Context:** [from the Project Context block — the full arc in 2-3 sentences]
**Last session:** [date, what was done]
**Progress:** X of Y tasks complete

### Where we left off:
[Last session's "where to pick up next time"]

### Next up:
- [ ] Task 1
- [ ] Task 2

### Blockers:
[Any noted blockers, or "None"]
```

### 4. Confirm Direction

Ask:
- "Ready to continue with [next task]?"
- "Or would you like to work on something else from the plan?"

When you're done working, run `/wrap` to save your progress.
