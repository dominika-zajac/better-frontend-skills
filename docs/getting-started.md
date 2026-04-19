# Getting started

This repository is a **collection of Agent Skills**: plain Markdown files with optional YAML frontmatter (`name`, `description`) that tell coding agents *how* to run a workflow consistently.

## Layout

Each skill lives in its own folder:

```text
skills/<skill-name>/SKILL.md
```

The `description` field in frontmatter is how agents (and humans) discover when a skill applies.

## Any agent, any editor

Skills are Markdown. You can paste them into system prompts, rules files, or notepads. For Cursor-specific paths, see [cursor-setup.md](cursor-setup.md).

## Related collections

This layout matches the pattern used by [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills): a top-level `skills/` directory with one `SKILL.md` per skill.
