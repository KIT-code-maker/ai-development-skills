# Landing Page Workflow

Purpose: create a polished, responsive landing page with an intentional visual narrative and optional scroll-driven animation / interactive 3D.

## Invocation
Use when asked to build or redesign a landing page, marketing page, promotional microsite, or scroll-based product story. Read the project's root `AGENTS.md` first. The library lives at `vendor/ai-development-skills/` if vendored; otherwise retrieve the applicable files from the linked GitHub repository. Workflows are orchestration instructions, not replacements for the original skills. Read each full `SKILL.md` and any relevant linked support files **at its stage**; do not load all skills into context at once.

## Choose a complexity tier
- **Standard**: static layout + CSS transitions / subtle entrance effects; avoid GSAP/Three.js unless already required. 
- **Motion** (default when scroll animation is specifically requested): animation choreography with GSAP Timeline / ScrollTrigger / React integration if React is present.
- **Immersive 3D**: adds a 3D scene only when the brief needs real-time 3D, shaders, particles, camera moves, or spatial interactions. Delegate the 3D production sequence to `workflows/interactive-3d.md`. Do not install an entire rendering stack for decorative motion alone.

## Non-negotiable guardrails
- Preserve an existing project's architecture and dependencies where possible; don't change frameworks just because React skills exist.
- Respect `prefers-reduced-motion` with usable content and non-motion alternatives. Make keyboard and touch interactions work.
- No unnecessary autoplay effects, excessive pinning, scroll-jacking or hidden content. Use responsive and low-performance fallbacks.
- Don't claim a preview, performance benchmark, visual audit or automated tests passed unless actually performed.
- The goal is to deliver real working code, not just a concept; checkpoints below are used for review. If the user explicitly asks to proceed end-to-end, proceed without waiting for approvals.

## Stage 0 — Understand brief and constraints
Inspect existing repo, routes, framework, scripts, content assets, typography, design system, analytics / SEO needs. Establish audience, CTA and narrative, target devices, content and performance constraints.
Output: one-page brief, proposed tier, section outline, technical assumptions and open risks.

## Stage 1 — Visual direction
Read `skills/frontend-design/SKILL.md`.
Define art direction, typography, spacing system, visual hierarchy, color use, image strategy, section-specific layout. Avoid generic template aesthetics and preserve brand constraints.
Output: section-by-section visual specification and content hierarchy.
Gate: direction is coherent, CTA accessible, layout accommodates mobile.

## Content-driven storytelling (project-specific when brief requests it)

For product or business-automation landing pages, use **semantic motion**: animations should illustrate what the current section explains, not serve as unrelated visual spectacle. Map each section to a system diagram or interaction and specify: meaning → displayed entities → state transitions → user or scroll trigger → accessible static fallback.

Example storyboards:
- Database/infrastructure: request flows from client → API gateway → backend → database, followed by query result/response; distinguish requests and responses.
- Integrations: two business systems exchange synchronized events, acknowledgements and updated states.
- Automation: trigger → conditional routing → task execution → successful result, with readable state changes.
- Analytics: input events aggregate into meaningful metrics and dashboard feedback. Never present simulated metrics as real live business data.
- AI-assisted processes: user input → validation → model/service processing → human checkpoint where appropriate → result, without inventing guarantees.

Start with an accessible static diagram with labels, then animate states on scroll using GSAP only when beneficial. Scroll controls animation **progress**, not logical accuracy. Prefer transforms/opacity, avoid jank and over-pinning; keep meaningful content visible without JavaScript and under `prefers-reduced-motion`. On touch / small screens, simplify nodes and timelines rather than compressing unreadable diagrams. Do not simulate real production data transfer or functional API calls unless a real backend is implemented and disclosed.

### Project font requirements

When the project's brief requests the Medeo family, use its actual licensed font assets in normal styles for readable body and informational copy; use an available verified pixelated/digital variant only as a selective technical accent (API, DB, FLOW, SYNC, labels, code-like diagrams). **Do not invent a Medeo Pixel font file or synthesize a font name.** If that exact variant is unavailable, ask for font assets where necessary or use a clearly identified licensed pixel-style fallback until supplied. Check Cyrillic glyph coverage, font licensing, preload strategy, FOIT/FOUT and mobile readability.

## Stage 2 — Implementation architecture
For React/Next.js, read `skills/react-best-practices/SKILL.md` and relevant `rules/` entries; otherwise follow the current project's stack.
Plan components, semantic HTML, assets, lazy loading, interaction state and reduced-motion paths.
Output: component and asset plan; implement static responsive page before complex animation.
Gate: all core content and CTAs usable without animation.

## Stage 3 — Motion storyboard
Read `skills/animations/SKILL.md` plus relevant rules in `skills/animations/rules/`.
Specify for each animated section: narrative meaning, data-flow accuracy, trigger, timeline, start/end scroll positions, scrub/pin behavior, easing, transform properties, layering, fallback and mobile behavior. Prioritize hierarchy and clarity over spectacle.
Output: motion table / storyboard.
Gate: no animation obscures CTAs or traps keyboard / scroll users.

## Stage 4 — Build animation
For Motion tier, read `skills/gsap-core/SKILL.md`, `skills/gsap-timeline/SKILL.md`, `skills/gsap-scrolltrigger/SKILL.md`; use `skills/gsap-react/SKILL.md` for React, `skills/gsap-frameworks/SKILL.md` when framework-specific.
Use GSAP only where it earns its complexity. Initialize after DOM is ready, clean up triggers on unmount, refresh when layout/assets change, scope selectors, handle resize and route changes. Protect scroll interaction and readability.
For Standard tier, prefer CSS and skip GSAP.
For Immersive 3D, execute `workflows/interactive-3d.md` and coordinate scene timeline with GSAP only after a baseline scene works.
Output: implemented transitions, scroll-linked sequences and reduced-motion fallback.
Gate: responsive, no obvious layout shift or sticky/pin collisions.

## Stage 5 — Polish and performance
Read `skills/gsap-performance/SKILL.md` for GSAP projects. Read applicable React performance rules. For 3D read `skills/threejs-performance/SKILL.md`.
Audit animation overhead, unnecessary style recalculations, layer count, asset sizes, images, font loading, mobile behavior. Test slower hardware / reduced motion if facilities permit.
Output: optimizations with observations / metrics only where measured.
Gate: no unhandled crashes, major jank, or inaccessible content; report unknowns.

## Stage 6 — UX audit and code review
Read `skills/web-design-guidelines/SKILL.md` and retrieve its rules from its specified upstream source (or the mirrored `upstream/web-interface-guidelines/command.md` if appropriate). Read `skills/requesting-code-review/SKILL.md` and its `code-reviewer.md`. Adapt subagent-specific procedure if subagents unavailable.
Run available build, lint, tests; inspect mobile + desktop if browser available. Report actionable findings and fix important issues.
Output: changed files, checks and results, limitations, remaining issues.

## Completion
Deliver implementation, brief list of decisions, tests performed, remaining limitations and instructions to run. Mention the skill files actually used, not imagined ones.
