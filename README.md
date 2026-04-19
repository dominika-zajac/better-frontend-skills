# better-frontend-skills

**Shareable Agent Skills for frontend quality work** (accessibility first; more topics may follow).

Each skill is a single `SKILL.md` with YAML frontmatter and a concrete workflow agents can follow.

---

## Quick start

Clone this repository (or add it as a submodule), then install the skills you need into your agent or editor. For **Cursor**, see [docs/cursor-setup.md](docs/cursor-setup.md). For a tool-agnostic overview, see [docs/getting-started.md](docs/getting-started.md).

```bash
git clone https://github.com/dominika-zajac/better-frontend-skills.git
cd better-frontend-skills
```

**Gemini CLI** (optional): install skills from the cloned repo path:

```bash
gemini skills install ./better-frontend-skills --path skills
```

---

## Skills

| Skill | What it does | When to use |
|-------|----------------|-------------|
| [accessibility-audit](skills/accessibility-audit/SKILL.md) | WCAG-oriented audits via Chrome DevTools MCP: Lighthouse (desktop + mobile), custom page scripts, keyboard focus, snapshot vs DOM parity, 320px reflow, touch targets, markdown report template | Auditing sites for accessibility, WCAG, Lighthouse/axe follow-ups, or Chrome DevTools MCP audit workflows |

---

## Repository structure

```text
better-frontend-skills/
├── skills/
│   └── accessibility-audit/
│       └── SKILL.md
├── docs/
│   ├── cursor-setup.md
│   └── getting-started.md
├── AGENTS.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

New skills should get their own directory under `skills/<name>/` with a `SKILL.md` inside. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

MIT — see [LICENSE](LICENSE).
