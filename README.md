# AI Design Skills

[![skills.sh](https://skills.sh/b/elayadesign/ai-design-skills)](https://skills.sh/elayadesign/ai-design-skills)

A focused supplemental Figma design skill for AI coding tools. General landing-page and frontend art direction is handled by the canonical Premium Frontend Director in `ThisismynameNOT/Claude`.

Each skill is a self-contained folder. Install the ones you need.

---

## Skills

| Skill | What it does |
|---|---|
| [`figma-designer`](./skills/figma-designer/SKILL.md) | Designs inside Figma with real structure: spacing, radius and color variables, named text styles, auto layout, components with every state, and a Foundations frame that updates with the tokens |

This personal fork deliberately excludes the conflicting global `landing-page-design` skill. The original remains recoverable from the backup branch `backup/skills-before-cleanup-20261113`.

<a href="https://slopscan.co"><img src="./assets/slopscan-banner.png" alt="SlopScan: audit your existing site. Checks a live page against these same rules and hands your agent a fix prompt." width="100%"></a>

---

## Install

Uses the [skills CLI](https://skills.sh). Needs Node.js.

```bash
npx skills add ThisismynameNOT/ai-design-skills
```

It lists the skills in this repo and asks which ones to install and for which agents. Add flags to skip the prompts:

```bash
# one skill
npx skills add ThisismynameNOT/ai-design-skills --skill figma-designer

# pick agents
npx skills add ThisismynameNOT/ai-design-skills -a claude-code -a cursor

# user-level instead of project-level
npx skills add ThisismynameNOT/ai-design-skills -g

# see what's available without installing
npx skills add ThisismynameNOT/ai-design-skills --list
```

Add `-y` to skip confirmations. Skills land in `.claude/skills/` for Claude Code and `.agents/skills/` for Cursor, Codex and other agents. Run `npx skills update` later to pull changes.

Then just ask, in plain language, for what the skill covers.

<details>
<summary><b>Manual install</b></summary>

Claude Code:

```bash
mkdir -p .claude/skills
git clone https://github.com/ThisismynameNOT/ai-design-skills.git /tmp/ai-design-skills
cp -r /tmp/ai-design-skills/skills/<skill-name> .claude/skills/
```

Cursor:

```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/<skill-name>.md \
  https://raw.githubusercontent.com/ThisismynameNOT/ai-design-skills/main/skills/<skill-name>/SKILL.md
```

Or paste the file into **Settings → Rules for AI**.

Codex, Windsurf, other: copy the skill's `SKILL.md` into your tool's rules file.

| Tool | Path |
|---|---|
| Codex | `AGENTS.md` |
| Windsurf | `.windsurfrules` |
| Cline | `.clinerules` |
| Generic | paste into your system prompt |
</details>

<details>
<summary><b>Claude.ai (no terminal)</b></summary>

Download the skill's `SKILL.md` and upload it to a Project, or attach it to a chat and say *"follow this."*
</details>

---

## Make it yours

Every skill's design values (fonts, colors, spacing, motion) live in one section near the bottom of its file. Fork this repo, edit that section, and the rest of the skill follows automatically.

---

## License

MIT. Use it, fork it, ship it, sell what you build with it. No attribution needed.
