# better-frontend-skills

**Shareable Agent Skills for frontend quality work** (accessibility first; more topics may follow).

Each skill is a single `SKILL.md` with YAML frontmatter and a concrete workflow agents can follow.

---

## Quick start

### Option A: [skills.sh](https://skills.sh/) CLI (recommended)

Install into your editor/agent using the open [skills](https://github.com/vercel-labs/skills) CLI ([docs](https://skills.sh/docs/cli)):

```bash
# Example: whole pack (you will be prompted for target agents)
npx skills add dominika-zajac/better-frontend-skills

# Example: only accessibility-audit, for Cursor, in current project
npx skills add dominika-zajac/better-frontend-skills --skill accessibility-audit --agent cursor
```

### Option B: Git clone

Clone this repository (or add it as a submodule), then copy or symlink skills as needed. For **Cursor** copy paths, see [docs/cursor-setup.md](docs/cursor-setup.md). For a tool-agnostic overview, see [docs/getting-started.md](docs/getting-started.md).

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

### Why `accessibility-audit`?

Lighthouse (and axe under the hood) catches many **mechanical** failures—contrast, missing labels, invalid ARIA, broken landmarks, and more—but real accessibility also depends on **content quality**, **keyboard behavior**, and **what assistive tech actually sees**. Agents often stop after a single Lighthouse run, which misses gaps that still block or confuse users.

The [accessibility-audit](skills/accessibility-audit/SKILL.md) skill gives the agent a **repeatable audit playbook** for Chrome DevTools MCP: desktop and mobile Lighthouse runs, then **extra checks Lighthouse does not do** (for example suspicious `alt` text, ambiguous link copy, broken skip-link targets, SVG naming, off-screen focusables, `aria-live` misuse, reduced-motion coverage). It adds **interactive verification** (Tab through the page, focus visibility, modals and focus traps), **DOM vs accessibility tree parity** (silent or “ghost” content, label mismatches), **320px reflow** with overflow detection, and **touch target** sizing after the mobile run—so you get closer to WCAG intent, not only automated scores.

It ends with a **standard markdown report template** and severity guidance, which makes findings easier to hand off, prioritize, or turn into tickets. If you already use `chrome-devtools-mcp`, this skill is the difference between a quick score and a structured, evidence-backed audit.

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
│   ├── getting-started.md
│   └── skills-sh.md
├── AGENTS.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

New skills should get their own directory under `skills/<name>/` with a `SKILL.md` inside. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License

MIT — see [LICENSE](LICENSE).
