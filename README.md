# UI Design Skill for Codex

Reusable `ui-design` skill package for Codex.

## Demo (One-shot)

- Live demo: `https://demo-codex-design.vercel.app`
- GitHub: `https://github.com/hursh-shah/demo-codex-design`

## What this skill does

`ui-design` helps Codex design and implement frontend UI directly in code (not just mockups).

Core behavior:

- Defaults to Next.js unless you explicitly request another framework
- Sets a clear visual direction before coding (tone, layout, typography, color, motion), using Anthropics frontend-design philosophy
- Uses targeted 21st.dev inspiration only for specific components when needed
- Prioritizes production-ready output: responsive layouts, accessibility states, and validation checks
- Enforces a Next.js security gate for `CVE-2025-55182` before implementation

Requirements for 21st.dev inspiration:

- The `screenshot` skill must be installed (used for component capture)
- Start Codex with search enabled: `codex --search`

## Install in Codex

Prerequisite: `skill-installer` is available (it is a built-in system skill in current Codex versions).

Install from this repo’s GitHub skill directory URL:

```bash
$skill-installer install https://github.com/<owner>/<repo>/tree/main/ui-design
```

After installing, restart Codex so the new skill is loaded.

## Skill folder

- `ui-design/` - skill package (`SKILL.md`, `agents/openai.yaml`, `references/`, `LICENSE.txt`)
