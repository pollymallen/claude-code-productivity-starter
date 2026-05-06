# /wrap — End Project Session

This is the "save game" command. Everything important from this session must be written to files before the conversation ends. **Do not ask questions.** Over-document rather than under-document — when in doubt, include it.

## Step 1: Review the session

Identify everything that happened: decisions made, files touched, features shipped, blockers hit, questions resolved, follow-ups created.

## Step 2: Update daily files

**TODAY.md:**
- Check off completed tasks with `[x]`
- Add new tasks that emerged during the session
- Set (or update) the ONE Thing for the next session

**WEEK.md:**
- Check off anything completed this week
- Add new tasks or deadlines that emerged
- Update "Promised to People" if any commitments changed

**BACKLOG.md** (if needed):
- Move new ideas or someday items here
- Update "Waiting On" if something is now blocked

## Step 3: Update project files

**PLAN.md — do not rush this:**
- Check off completed items with `[x]`
- Add new tasks that emerged
- Remove dead tasks
- Update status lines
- Sanity-check that the plan reflects reality

**SESSION-LOG.md** (create it if it doesn't exist):

Add a dated session entry with:
- What was done
- What's unfinished
- Where to pick up next time
- Any decisions, URLs, file paths, or context that would be lost if the conversation disappeared

**Archive old sessions:** If SESSION-LOG.md has more than 3 session entries, move all but the last 2 to a `SESSION-ARCHIVE.md` file in the same folder.

**Project Context block:** At the top of SESSION-LOG.md, maintain a dense 3-5 sentence summary called `## Project Context` that covers the full arc of the project from session 1 forward. Update this every session. This is what `/resume-project` reads first to get oriented — it should be enough to understand the project cold.

## Step 4: Update PORTFOLIO.md

Go back to the system root and update `PORTFOLIO.md`:
- Update this project's status and "Next" action
- Move to "Done" section if the project is complete

## Step 5: Summary

Two sentences: what we accomplished and what's most important next time.

**Remind the user that the usual next step is `/clear` then `/resume-project` when they're ready to work again. Don't execute those yourself.**
