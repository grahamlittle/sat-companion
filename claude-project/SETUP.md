# Setup — claude.ai (Projects)

This is the easiest path. No installation. About five minutes.

A **Project** on claude.ai is a saved workspace with its own instructions and knowledge files. We turn SAT Companion into a Project so every new chat inside it is already a Digital SAT coach.

## Prerequisites

- A **claude.ai** account. Projects are available on paid plans (Pro/Team); check your plan if you do not see the Projects option.

## Steps

1. On claude.ai, open the sidebar and click **Projects**, then **Create project**. Name it **SAT Companion**.

2. Open the project's **Instructions** (sometimes labelled "Set custom instructions" or "What are you working on?"). Copy the **entire contents** of [`project-instructions.md`](project-instructions.md) and paste it in. Save.

3. Add the reference material as **knowledge**. Click **Add content** / the knowledge (paperclip) area and upload these four files from the skill's `references/` folder (in this bundle at `../skill/sat-companion/references/`):
   - `test-structure.md`
   - `reading-writing.md`
   - `math.md`
   - `scoring-and-strategy.md`

   The instructions tell Claude to consult these by name, so the filenames must stay as-is.

4. Start a new chat **inside the project** and test: *"Digital SAT Reading & Writing — here's a Transitions question I'm unsure about. Walk me through it, don't just give the letter."* Claude should respond as the SAT coach and end with the `(SAT Companion — Last Updated: September 2026)` footer.

## Tips for students

- Always chat **inside the project** — chats started outside it will not have the coach set up.
- Paste a question you got wrong and *your* reasoning for the choice you made. The coach diagnoses the misconception instead of just correcting it.
- Tell it your test date, current or diagnostic score, and target up front — it tailors the plan to the gap.

## Keeping it current

If the reference files are updated later, delete the old knowledge files and re-upload the new ones. Update the instructions only if `project-instructions.md` changes.
