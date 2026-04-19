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

## skills.sh / `npx skills` compatibility

Keep each skill as `skills/<name>/SKILL.md` with valid YAML `name` and `description` so the [skills](https://github.com/vercel-labs/skills) CLI ([skills.sh](https://skills.sh/)) can discover and install it. After adding a skill, document it in `README.md` and optionally add install one-liners to `docs/skills-sh.md`.

Pull requests should explain the workflow the skill encodes and any tools (MCP, CLIs) it assumes.
