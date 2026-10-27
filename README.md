# AI Development Skills

Complete upstream Agent Skills copied verbatim, with their referenced supporting files.

## Sources

- `skills/frontend-design/` — https://github.com/anthropics/skills/tree/main/skills/frontend-design
- `skills/web-design-guidelines/` — https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines
- `skills/react-best-practices/` — https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices
- `skills/requesting-code-review/` — https://github.com/obra/superpowers/tree/main/skills/requesting-code-review
- `skills/python-pro/` — https://github.com/Jeffallan/claude-skills/tree/main/skills/python-pro
- `skills/fastapi-expert/` — https://github.com/Jeffallan/claude-skills/tree/main/skills/fastapi-expert
- `skills/animations/` — https://github.com/mthines/agent-skills/tree/main/skills/design/animations
- `skills/gsap-*/` — https://github.com/greensock/gsap-skills/tree/main/skills
- `skills/threejs-*/` — https://github.com/cesartevisual/threejs-skills/tree/main/skills

Additional mirrored source: `upstream/web-interface-guidelines/` from https://github.com/vercel-labs/web-interface-guidelines — the Vercel UI audit skill fetches these rules dynamically.

The upstream skill files are not modified. Consult each source's license terms; available additional licenses are saved in `upstream/licenses/`. Revisit licensing before redistributing.

## Use in other repositories

Copy [`templates/AGENTS.md`](templates/AGENTS.md) into your project's root as `AGENTS.md`.

**Recommended reliable integration:**

```bash
git submodule add https://github.com/KIT-code-maker/ai-development-skills.git vendor/ai-development-skills
git add .gitmodules vendor/ai-development-skills AGENTS.md
git commit -m "Connect shared Agent Skills"
```

The agent should load the relevant `SKILL.md` under `vendor/ai-development-skills/skills/` and any linked references. For a clone, initialize with `git submodule update --init --recursive`. A GitHub URL in AGENTS.md **does not automatically install or execute** a skill. Submodule commits remain pinned until manually updated.
