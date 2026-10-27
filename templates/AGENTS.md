# Project Agent Instructions

## Shared Agent Skills library

Canonical repository: https://github.com/KIT-code-maker/ai-development-skills

Before starting any code or UI task:
1. Read this file and inspect the project's existing conventions.
2. Locate the shared skill library, preferably at `vendor/ai-development-skills/skills/` (a Git submodule, pinned to a reviewed commit).
3. If the library isn't vendored, use the connected GitHub repository to fetch the relevant **complete** `SKILL.md` and referenced `rules/`, `references/`, or `templates/` files. A URL alone is not a loaded skill.
4. Choose only the relevant skills below, read their `SKILL.md` first, then read any referenced supporting files required by the task. Never pretend a remote file was loaded if it was inaccessible.
5. Respect existing design, dependencies, behavior and project constraints. Avoid unrelated changes.
6. Run available tests, formatting and linting. Report any checks not run.

## Workflow selection (before choosing individual skills)

For a substantial multi-stage task, inspect and read **one** primary workflow from the shared library:
- Copy, positioning, offers, audience research, headlines, website content → `workflows/content-strategy.md`. Complete and approve content before visual work when requested.
- New landing page, marketing microsite, scroll-driven product page → `workflows/landing-page.md`.
- Interactive 3D scene, shaders, particles or complex WebGL interaction → `workflows/interactive-3d.md`; when part of a landing page, follow the landing-page workflow and invoke the 3D workflow at its scene stage.
- Dashboard, Telegram Mini App, backend-enabled site or multi-screen application → `workflows/web-app.md`.

Locate workflow files under `vendor/ai-development-skills/workflows/` when vendored; otherwise fetch from the connected GitHub repository. **A Markdown link alone does not load a workflow.**

Use the workflow's stages and checkpoints in order. Load only the skills called for by the current stage, including relevant rule/reference files. Do not prematurely load all 39 skills, claim unseen files were read, or hold for approval if the user's request already authorizes end-to-end work. Small bug fixes can use only directly relevant skills without a full workflow.

## Business automation landing specialization

If the project is a landing page for business automation services, use the specialized project kit:
- `templates/business-automation-landing/AGENTS.md` — copy this to the **project root** as `AGENTS.md` (it includes skill routing, project-specific instructions and font usage).
- `templates/business-automation-landing/PROJECT_BRIEF.md` — positioning, section narratives and constraints.
- `templates/business-automation-landing/MOTION_STORYBOARD.md` — concrete scroll-linked interactive scenes.

These design preferences (including the Medeo type system) are specific to this landing concept; **do not apply them to unrelated projects by default**. In an existing project, use the specialized template instead of blindly appending conflicting root instructions. Keep sources accessible with a pinned submodule or supported GitHub file access.

## Existing project / redesign policy

If files, components, mockups, styles, content or animations already exist, begin with an **inventory and audit** rather than starting from a blank page. Identify what works, the existing font/color tokens, existing GSAP/React infrastructure, uncommitted work (if visible), dependencies and behavior to preserve. Reuse and improve the existing implementation unless an explicit rebuild was requested. Present a concise improvement plan, then apply incremental changes. Do not overwrite user-created work, remove content, replace project architecture, or change public APIs without necessity. Run available checks and explain what changed.

For visual identity and palette choices, read `skills/design-excellence/SKILL.md` and `skills/color-system/SKILL.md`, plus the relevant `skills/color-system/references/` documents. Their suggested defaults are advisory: project brand, actual licensed fonts (e.g. Medeo), accessibility and existing design constraints take precedence over generic color or typography prescriptions.

## Task → skill routing

| Task | Skill directory relative to library's `skills/` |
|---|---|
| Customer research and evidence-backed audience hypotheses | `customer-research/` |
| Positioning, offer definition and value proposition | `offers/` |
| Landing page headlines, section copy and CTAs | `copywriting/` |
| Copy quality, clarity and AI-cliché removal | `copy-editing/` |
| Anti-generic visual quality and design audit | `design-excellence/` |
| Semantic palette, color tokens, contrast and color harmony | `color-system/` and relevant `references/` |
| Design new page or improve visual composition | `frontend-design/` |
| Accessibility, usability, interface audit | `web-design-guidelines/` |
| React and Next.js performance, architecture | `react-best-practices/` |
| Verify changes, review PRs and diffs | `requesting-code-review/` |
| Python code, typing, async, tests | `python-pro/` |
| FastAPI API endpoints, Pydantic, SQLAlchemy | `fastapi-expert/` |
| CSS, interaction motion, transitions and animation decisions | `animations/` |
| GSAP timeline and scroll-driven animation | `gsap-core/`, `gsap-timeline/`, `gsap-scrolltrigger/`; optionally `gsap-react/`, `gsap-performance/`, `gsap-plugins/`, `gsap-frameworks/`, `gsap-utils/` |
| Three.js/WebGL/WebGPU, shaders, particles and 3D scenes | Choose the relevant `threejs-*/` skills, including `threejs-r3f/`, `threejs-shaders/`, `threejs-particles/`, `threejs-performance/` |

## Guidelines

- Prefer restrained, task-appropriate animation to gratuitous effects; honor reduced-motion preferences.
- Do not bring GSAP or Three.js into an existing project unless the task benefits and the change is approved by requirements.
- Preserve original upstream skill files. Project-specific overrides belong in this file.
- Do not execute scripts copied from third-party repositories without inspecting their behavior.
- If the skill library is not available, explain the limitation and proceed using project rules rather than guessing skill contents.
