# AGENTS.md — Business Automation Landing Page

This is a **project-specific** agent instruction file for a premium landing page offering business process automation, integrations, data infrastructure, AI-assisted workflows and custom internal tools. In the target project place this file at the **root** as `AGENTS.md`. Keep `docs/PROJECT_BRIEF.md` and `docs/MOTION_STORYBOARD.md` adjacent under `docs/`.

## Authoritative project documents
1. Read `docs/PROJECT_BRIEF.md` first for positioning, customer claims and page scope.
2. Read `docs/MOTION_STORYBOARD.md` for visual explanations tied to scroll progression.
3. Inspect existing repository structure and actual font assets before writing code.
4. Load `workflows/landing-page.md` from https://github.com/KIT-code-maker/ai-development-skills (vendored: `vendor/ai-development-skills/workflows/landing-page.md`). Choose the **Motion** tier by default, escalating to Immersive 3D only when explicitly justified.
5. At each workflow stage load only the corresponding full upstream `SKILL.md` and its relevant reference files from `vendor/ai-development-skills/skills/` or from the connected GitHub repository. A URL does not by itself mean the content has been read.

## Skills sequence
- Art direction → `frontend-design/`
- React implementation (only if project uses React) → `react-best-practices/` with relevant `rules/`
- Motion storyboard → `animations/` and relevant `rules/`
- Scroll scenes → `gsap-core/`, `gsap-timeline/`, `gsap-scrolltrigger/`, and `gsap-react/` if React
- Performance → `gsap-performance/` and framework performance references
- Optional actual real-time 3D → relevant `threejs-*/` and `workflows/interactive-3d.md`
- Audit → `web-design-guidelines/`, `requesting-code-review/` (including `code-reviewer.md`)

## Typography: Medeo
- Use genuine **Medeo** assets in their provided licensed weights/styles, not invented filenames or invented weights.
- Standard/non-pixel Medeo: body paragraphs, informational text, menus, buttons and primary accessible copy.
- Pixelated/digital Medeo variant, **if a real asset with proper rights and Cyrillic support is supplied**: selective IT accents only — DB/API/backend/status labels, short captions, system tokens, technical callouts.
- Hero typography may mix the two treatments sparingly; long text must stay conventional and legible.
- If the pixel variant is not an actual available Medeo face, do not claim that it exists; document the missing asset and use an approved licensed pixel-style fallback as temporary technical accent.
- Declare explicit `@font-face` based on inspected files; prefer WOFF2 and load only needed weights/subsets. Check Cyrillic, licensing and `font-display`.
- Do not commit commercial font binaries to a public repository unless redistribution is authorized.

## Direction
Modern, structured, technologically literate and premium. No generic neon overload, random floating cards, stock AI brains, fake command-line wallpaper or effects disconnected from meaning. Visual confidence comes from typography, rhythm, precise diagrams, restraint and coherent motion.

## Section-linked visuals
**Every section's animation must teach or reinforce that section's actual process.**
- DB / backend → client request → API → service/backend → query → database → response; identifiable request and reply states
- Automation → input trigger → validation → conditional route → action → visible outcome
- Integrations → system A ↔ connector → system B, event delivery and acknowledgement
- Dashboards / analytics → raw events → aggregation → updated labeled chart or metric (demo data clearly marked)
- AI → request/context → model/service → validation/human review where applicable → useful result; avoid misleading autonomous promises

The storyteller is the product process, not the scroll effect. Use scroll progress to reveal sequence; never make readable content depend exclusively on a user completing an animation.

## Engineering and acceptance criteria
- Semantic, responsive, keyboard-operable, reduced-motion compatible; mobile scenes degrade to compact readable static/step variants.
- No fake functional integrations or claims; simulated diagrams must be labeled as illustrations.
- Do not add Three.js unless a real spatial illustration demands it; prefer SVG + CSS/GSAP for network diagrams.
- Build the static accessible landing page and content first, animate second, optimize and review last.
- Clean up GSAP contexts/ScrollTriggers on navigation and unmount; handle resize, dynamic font/image loading, and pin positions.
- Keep motion primarily on transforms/opacity; budget media/assets carefully and avoid inaccessible scroll-jacking.
- Run available checks (build, lint, tests). Never claim results you did not verify.
- Summarize per-stage deliverables and remaining assumptions. When authorized for end-to-end work, proceed through the stages without waiting for repeated approval.
