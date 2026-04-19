# Using better-frontend-skills with Cursor

## Option 1: Project rules (recommended for one repo)

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

## Option 3: Git submodule

In a project where you want the pack versioned:

```bash
git submodule add https://github.com/<YOUR_ORG>/better-frontend-skills.git third_party/better-frontend-skills
mkdir -p .cursor/rules
cp third_party/better-frontend-skills/skills/accessibility-audit/SKILL.md .cursor/rules/accessibility-audit.md
```

## Usage tips

- Do not load every skill as an always-on rule if the pack grows; use a few rules and reference others when needed.
- Mention the skill in chat when you want it applied explicitly (for example: “Follow the accessibility-audit skill for this URL”).
