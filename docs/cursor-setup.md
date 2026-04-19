# Using better-frontend-skills with Cursor

## Option 0: skills CLI ([skills.sh](https://skills.sh/))

The [skills](https://github.com/vercel-labs/skills) CLI can install straight from GitHub into the paths Cursor uses (for example `.agents/skills/` in the project, or `~/.cursor/skills/` when global).

```bash
npx skills add dominika-zajac/better-frontend-skills --skill accessibility-audit --agent cursor
```

Use `-g` for a user-wide install. See [skills-sh.md](skills-sh.md) for full examples, deep links, and `DISABLE_TELEMETRY=1`.

## Option 1: Project rules (manual copy)

Copy the skill into `.cursor/rules/` so it loads with that project (rename optional):

```bash
mkdir -p .cursor/rules
cp path/to/better-frontend-skills/skills/accessibility-audit/SKILL.md .cursor/rules/accessibility-audit.md
```

## Option 2: Personal skills (all projects on this machine)

Cursor loads personal skills from `~/.cursor/skills/<skill-name>/SKILL.md`.

```bash
mkdir -p ~/.cursor/skills/accessibility-audit
cp path/to/better-frontend-skills/skills/accessibility-audit/SKILL.md ~/.cursor/skills/accessibility-audit/SKILL.md
```

To track updates from git without copying, symlink the folder (adjust paths):

```bash
ln -s "$(pwd)/better-frontend-skills/skills/accessibility-audit" ~/.cursor/skills/accessibility-audit
```

## Usage tips

- Do not load every skill as an always-on rule if the pack grows; use a few rules and reference others when needed.
- Mention the skill in chat when you want it applied explicitly (for example: “Follow the accessibility-audit skill for this URL”).
