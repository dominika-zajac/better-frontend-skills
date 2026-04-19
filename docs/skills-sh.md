# Install via [skills.sh](https://skills.sh/) (Open Agent Skills)

The [skills](https://github.com/vercel-labs/skills) CLI is the install path surfaced on [skills.sh](https://skills.sh/) and in the [CLI documentation](https://skills.sh/docs/cli). It discovers skill packs that use a `skills/` directory with one `SKILL.md` per folder (same layout as this repository).

## Prerequisites

- Node.js (for `npx`)
- A **public** GitHub repository if you want others to install with `owner/repo` shorthand

## Install this pack

From a project directory (default: install into that project’s agent skill paths):

```bash
npx skills add dominika-zajac/better-frontend-skills
```

Replace `dominika-zajac` with your fork’s owner if different.

### Install only one skill

```bash
npx skills add dominika-zajac/better-frontend-skills --skill accessibility-audit
```

### Install for Cursor only

```bash
npx skills add dominika-zajac/better-frontend-skills --skill accessibility-audit --agent cursor
```

### Global install (all projects on this machine)

```bash
npx skills add dominika-zajac/better-frontend-skills --skill accessibility-audit -g --agent cursor
```

### Full GitHub URL or deep link

```bash
npx skills add https://github.com/dominika-zajac/better-frontend-skills
npx skills add https://github.com/dominika-zajac/better-frontend-skills/tree/main/skills/accessibility-audit
```

### List skills in the repo without installing

```bash
npx skills add dominika-zajac/better-frontend-skills --list
```

## How this relates to the skills.sh directory

- **Discovery**: Browse and search at [skills.sh](https://skills.sh/).
- **Ranking**: The CLI collects **anonymous** install telemetry to build the leaderboard ([docs](https://skills.sh/docs)). No personal data; see the site’s security notes.
- **Opt out of telemetry**: set `DISABLE_TELEMETRY=1` in your environment when running `npx skills`.

There is no separate “registration” step for this repo: once it is public on GitHub and people run `npx skills add …`, usage can contribute to visibility on the leaderboard over time.

## Compatibility

This pack follows the layout the CLI searches for (see [vercel-labs/skills](https://github.com/vercel-labs/skills) README): each skill is `skills/<skill-name>/SKILL.md` with valid YAML `name` and `description` in the frontmatter.

## Further reading

- [skills.sh documentation](https://skills.sh/docs)
- [Cursor skills in Cursor Docs](https://cursor.com/docs/context/skills) (conceptual; paths may match `~/.cursor/skills/` when using global install)
