# Design Pressure Test

[![skills.sh](https://skills.sh/b/pkshefi/design-pressure-test-skill)](https://skills.sh/pkshefi/design-pressure-test-skill)
[![License: MIT](https://img.shields.io/badge/License-MIT-black.svg)](./LICENSE)

A whitespace and spacing audit skill for AI coding agents. Pressure-tests every spacing decision in a UI design and returns specific pixel adjustments tied to Tailwind / shadcn spacing tokens.

> Made by **Mohammed Shafeeq (Mosh)** · [mosh.fyi](https://mosh.fyi) · [@pkshefi](https://github.com/pkshefi)

## Install

One command, any supported agent:

```bash
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test
```

The installer detects your agents and copies the skill into the right directory. Add `-g` to install globally across projects.

### Install for a specific agent

```bash
# Claude Code
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a claude-code

# Cursor
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a cursor

# Codex
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a codex

# GitHub Copilot
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a github-copilot

# Gemini CLI
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a gemini-cli

# Windsurf
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a windsurf

# OpenCode
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a opencode

# Roo Code
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a roo

# Cline
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a cline

# Kilo Code
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a kilo

# Amp / Replit
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a amp

# Antigravity
npx skills add pkshefi/design-pressure-test-skill --skill design-pressure-test -a antigravity
```

See the full agent list at [skills.sh/docs/agents](https://skills.sh/docs).

### Manual install

Copy `skills/design-pressure-test/` into your agent's skills directory:

| Agent | Project path | Global path |
| --- | --- | --- |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` |
| Cursor | `.agents/skills/` | `~/.cursor/skills/` |
| Codex, Copilot, Gemini CLI, OpenCode, Windsurf, Cline, Roo, Kilo, Amp, Zed | `.agents/skills/` | `~/.agents/skills/` |
| Kiro CLI | `.kiro/skills/` | `~/.kiro/skills/` |
| Trae | `.trae/skills/` | `~/.trae/skills/` |

## Usage

Ask your agent to pressure-test your design:

> "Run the design pressure test on this landing page"
> "Audit the whitespace in this component"
> "Review the spacing — it feels cramped"
> "Why does this pricing table feel cheap?"

The skill analyzes:

- **Macro Spacing** — section gaps, spatial rhythm, 8pt grid consistency
- **Micro Spacing** — card padding, icon clearance, button padding, line-height
- **Breathing Room** — isolation of important elements, intentional whitespace
- **Perceived Value** — premium padding mapping, density reduction

## Output

Every audit produces a structured report with:

1. **Summary Score** (1–10)
2. **Critical Issues**
3. **Quick Wins**
4. **Structural Changes**
5. **Pixel Map** — specific old/new values with Tailwind / shadcn token changes

Example pixel map:

| Element | Current | Recommended | Token change |
| --- | --- | --- | --- |
| Hero section padding | 24px | 96px top, 64px bottom | `p-6` → `pt-24 pb-16` |
| Card inner padding | 24px | 40px | `p-6` → `p-10` |
| Feature grid gap | 0 | 32px | `gap-0` → `gap-8` |
| Button horizontal | 12px | 20px | `px-3` → `px-5` |

## Repository structure

```
skills/design-pressure-test/
├── SKILL.md                 # Skill definition and audit framework
├── references/
│   ├── patterns.md          # Hero, card, form and grid spacing patterns
│   ├── sharp_edges.md       # Common spacing failures and fixes
│   └── validations.md       # Machine-readable regex checks
└── evals/
    └── evals.json           # Behavioural test prompts and assertions
skills.sh.json               # Skills directory grouping metadata
```

## Compatibility

Works with any agent that supports the [Agent Skills specification](https://agentskills.io), including Claude Code, Cursor, Codex, GitHub Copilot, Gemini CLI, Windsurf, OpenCode, Cline, Roo Code, Kilo Code, Amp, Antigravity, Kiro CLI, Trae, Zed and 60+ more.

## License

[MIT](./LICENSE) © Mohammed Shafeeq (Mosh) — mosh.fyi
