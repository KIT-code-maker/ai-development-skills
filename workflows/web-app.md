# Web Application Workflow

Use for an interactive site, dashboard, Telegram Mini App, or full-stack web application with real product flows. Not intended for pure marketing landing pages (use `workflows/landing-page.md`).

1. **Discover** — Inspect repository, users, data, auth, integrations, dependencies, deployment and existing behavior. Write acceptance criteria and identify regressions to avoid.
2. **Design flows** — Read `skills/frontend-design/SKILL.md` for new UI, and `skills/web-design-guidelines/SKILL.md` for design review. Define navigation, loading/empty/error states, mobile responsiveness and accessibility.
3. **Architect** — For React/Next.js read `skills/react-best-practices/SKILL.md` and relevant `rules/`. For Python read `skills/python-pro/SKILL.md`; for FastAPI additionally read `skills/fastapi-expert/SKILL.md` and relevant references. Do not impose any of these stacks on an unrelated existing project. Plan API contracts, models, migrations and security boundaries.
4. **Implement vertical slices** — Deliver one working flow at a time. Keep server/client interfaces aligned; preserve stored data; test migrations before applying them to live environments. Never place secrets in repository or log them.
5. **Motion only when useful** — For UI interactions read `skills/animations/SKILL.md`. Use GSAP Skills for specifically required complex timeline / scroll effects. 3D requests are delegated to `workflows/interactive-3d.md`.
6. **Validate** — Run relevant unit, integration, API and frontend tests and lint/build checks. Read `skills/web-design-guidelines/SKILL.md` for UI audit and `skills/requesting-code-review/SKILL.md` + `code-reviewer.md` before merge. Inspect permissions, data integrity, accessibility and error handling.
7. **Deliver** — Document changed files, acceptance criteria met, checks performed, manual actions needed, any unknowns and risks.

Load skills just-in-time; read a full skill and linked supporting files before applying it, not all available skills simultaneously.
