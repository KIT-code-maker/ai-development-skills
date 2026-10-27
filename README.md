# AI Development Skills

Complete upstream Agent Skills copied verbatim, with their referenced supporting files.

## Sources

- `skills/customer-research/`, `skills/offers/`, `skills/copywriting/`, `skills/copy-editing/` — https://github.com/coreyhaines31/marketingskills/tree/main/skills (full original directories including references and evals)
- `skills/frontend-design/` — https://github.com/anthropics/skills/tree/main/skills/frontend-design
- `skills/web-design-guidelines/` — https://github.com/vercel-labs/agent-skills/tree/main/skills/web-design-guidelines
- `skills/react-best-practices/` — https://github.com/vercel-labs/agent-skills/tree/main/skills/react-best-practices
- `skills/requesting-code-review/` — https://github.com/obra/superpowers/tree/main/skills/requesting-code-review
- `skills/python-pro/` — https://github.com/Jeffallan/claude-skills/tree/main/skills/python-pro
- `skills/fastapi-expert/` — https://github.com/Jeffallan/claude-skills/tree/main/skills/fastapi-expert
- `skills/design-excellence/` — https://github.com/majiayu000/claude-skill-registry-data/blob/a21980a5b576646393ed574f158d7dd92fae4c3f/data/design-excellence/SKILL.md (archived source snapshot; original content preserved)
- `skills/color-system/` — https://github.com/AntJanus/skillbox/tree/main/skills/color-system
- `skills/animations/` — https://github.com/mthines/agent-skills/tree/main/skills/design/animations
- `skills/gsap-*/` — https://github.com/greensock/gsap-skills/tree/main/skills
- `skills/threejs-*/` — https://github.com/cesartevisual/threejs-skills/tree/main/skills

Additional mirrored source: `upstream/web-interface-guidelines/` from https://github.com/vercel-labs/web-interface-guidelines — the Vercel UI audit skill fetches these rules dynamically.

The upstream skill files are not modified. Consult each source's license terms; available additional licenses are saved in `upstream/licenses/`. Revisit licensing before redistributing.

## Visual identity and existing drafts

The landing workflow now includes a `Stage 1b` using complete `design-excellence` and `color-system` Skills. New projects get a deliberate palette and semantic tokens; existing designs receive a code/design audit and **incremental enhancement**, preserving user-authored content, architecture and working behavior. Generic defaults from third-party Skills do not override project-specific brand requirements such as Medeo.

## Workflows

Select an end-to-end process **before** individual skills:

- [Content Strategy](workflows/content-strategy.md): customer research → offers → copywriting → copy editing → content/visual map. This precedes visual production when copy isn't approved.
- [Landing Page](workflows/landing-page.md): standard, scroll-motion, or immersive 3D landing pages.
- [Interactive 3D](workflows/interactive-3d.md): 3D scenes, shaders, particles and scroll-linked camera moves.
- [Web App](workflows/web-app.md): full-stack applications, dashboards and Telegram Mini Apps.

The [AGENTS.md template](templates/AGENTS.md) now routes projects to the appropriate workflow and then loads relevant complete upstream skill files at each stage. These workflows and templates are project orchestration instructions; the upstream `skills/` files remain unmodified.

## Business automation landing starter

For the specific business automation landing page concept, use the complete [project kit](templates/business-automation-landing/):

- [Root project `AGENTS.md`](templates/business-automation-landing/AGENTS.md) — Medeo typography, content-driven graphics, skill/workflow selection.
- [`PROJECT_BRIEF.md`](templates/business-automation-landing/PROJECT_BRIEF.md) — audience, value proposition, sections, calls to action, design constraints.
- [`MOTION_STORYBOARD.md`](templates/business-automation-landing/MOTION_STORYBOARD.md) — scroll choreography for databases, integrations, workflows, AI and analytics.

Copy all three files into the new project's root (with the two supporting documents under `docs/` as instructed). This kit is opt-in and does not impose Medeo on unrelated applications.

## Use in other repositories

Copy [`templates/AGENTS.md`](templates/AGENTS.md) into your project's root as `AGENTS.md`.

**Recommended reliable integration:**

```bash
git submodule add https://github.com/KIT-code-maker/ai-development-skills.git vendor/ai-development-skills
git add .gitmodules vendor/ai-development-skills AGENTS.md
git commit -m "Connect shared Agent Skills"
```

The agent should load the relevant `SKILL.md` under `vendor/ai-development-skills/skills/` and any linked references. For a clone, initialize with `git submodule update --init --recursive`. A GitHub URL in AGENTS.md **does not automatically install or execute** a skill. Submodule commits remain pinned until manually updated.
