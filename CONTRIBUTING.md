# Contributing

## Adding a skill

1. Create a directory under `skills/` using a **lowercase hyphenated** name (for example, `skills/performance-budgets/`).
2. Add `SKILL.md` with YAML frontmatter at the top:

   ```yaml
   ---
   name: performance-budgets
   description: Third-person description of what the skill does and when the agent should use it (include trigger terms).
   ---
   ```

3. Keep `SKILL.md` focused and actionable; put long reference material in sibling files (for example, `reference.md`) and link from `SKILL.md`.
4. Update the skills table in `README.md` and, if setup steps differ, extend `docs/cursor-setup.md`, `docs/getting-started.md`, or [docs/skills-sh.md](docs/skills-sh.md).

## Inter-skill dependencies

Skills may reference and depend on other skills in this repository. When a skill requires another skill as a prerequisite or calls into its workflow (for example, `accessibility-fix` depends on `accessibility-audit` to produce its input and re-runs it for verification), document the dependency explicitly:

1. Add a blockquote note near the top of the dependent skill's `SKILL.md` linking to the prerequisite (for example: `> **Related skill**: \`accessibility-audit\` — run this first if you do not already have a report.`).
2. Add a forward pointer in the prerequisite skill pointing to the dependent (for example: `> **Next step**: use the \`accessibility-fix\` skill to apply fixes.`).
3. Describe the dependency in the skills table in `README.md` so users understand the intended workflow order.

## skills.sh / `npx skills` compatibility

Keep each skill as `skills/<name>/SKILL.md` with valid YAML `name` and `description` so the [skills](https://github.com/vercel-labs/skills) CLI ([skills.sh](https://skills.sh/)) can discover and install it. After adding a skill, document it in `README.md` and optionally add install one-liners to `docs/skills-sh.md`.

Pull requests should explain the workflow the skill encodes, any tools (MCP, CLIs) it assumes, and any other skills it depends on.
