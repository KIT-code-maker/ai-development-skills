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

## Task → skill routing

| Task | Skill directory relative to library's `skills/` |
|---|---|
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
