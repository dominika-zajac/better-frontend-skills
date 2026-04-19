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
4. Update the skills table in `README.md` and, if setup steps differ, extend `docs/cursor-setup.md` or `docs/getting-started.md`.

Pull requests should explain the workflow the skill encodes and any tools (MCP, CLIs) it assumes.
