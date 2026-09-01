# Setup — Claude Code (CLI or desktop app)

This path installs SAT Companion as a native **Skill**. Claude Code loads it automatically whenever you ask a Digital SAT question.

## Prerequisites

- **Claude Code** installed (the CLI, or the Claude desktop/web app that supports skills).
- Basic comfort with copying a folder into a directory.

## Install

1. Copy the `sat-companion/` folder (the one inside this `skill/` directory — it contains `SKILL.md` and a `references/` folder) into your skills directory:

   - **Personal skills (all projects):** `~/.claude/skills/`
   - **Project-only skill:** `.claude/skills/` inside a specific project.

   The result should look like:
   ```
   ~/.claude/skills/sat-companion/
     SKILL.md
     references/
       test-structure.md
       reading-writing.md
       math.md
       scoring-and-strategy.md
   ```

2. Start (or restart) Claude Code so it picks up the new skill.

3. Test it: ask *"Digital SAT Math — here's a linear-systems question I got wrong. Don't tell me the answer, help me see my mistake."* Claude should adopt the SAT coach role and end its reply with the `(SAT Companion — Last Updated: September 2026)` footer.

## How it loads

You do **not** call the skill manually. `SKILL.md` has a description that tells Claude to invoke it for any Digital SAT question. The `references/` files load on demand — e.g. the Math reference only loads when you ask about Math — which keeps context lean.

## Updating

Replace the folder with a newer version and restart. Everything is plain Markdown, so you can also edit `SKILL.md` or the references directly. The test details reflect the current Digital SAT — re-check satsuite.collegeboard.org if the College Board publishes a change, or run the `/update-sat-companion` skill.
