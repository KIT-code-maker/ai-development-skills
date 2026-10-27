# Content Strategy Workflow

Purpose: develop accurate and differentiated B2B website messaging **before** deciding visual storytelling, layout and animations. Apply to new marketing pages and content-focused revisions.

## Invocation & source skills
Start from the project's root `AGENTS.md`, read existing content, `docs/PROJECT_BRIEF.md` if present, and any `.agents/product-marketing.md` project context. Load original skills from `vendor/ai-development-skills/skills/`, or retrieve via connected GitHub when available. Read the **complete** `SKILL.md` and relevant references just-in-time, rather than loading all skills at once:
1. `skills/customer-research/SKILL.md` (+ applicable `references/`)
2. `skills/offers/SKILL.md` (+ applicable `references/`)
3. `skills/copywriting/SKILL.md` (+ `references/ai-tells.md`, `copy-frameworks.md`, `natural-transitions.md` when useful)
4. `skills/copy-editing/SKILL.md` (+ applicable `references/`)

These are original upstream instructions. This workflow coordinates them; it does not replace or edit them.

## Stage 0 — Existing content inventory
Read project pages, drafts, existing approved headlines, navigation, CTAs, FAQs, previous positioning, content sources and any evidence of actual products or services. Categorize as confirmed, plausible but unverified, or unknown. **Preserve existing approved copy** by default. Keep the already-approved section “Разрозненные задачи. Согласованная работа.” and its three inputs → processing logic → two outcomes in the business automation project unless user explicitly asks to change it.
Deliver: copy inventory, gaps and claims ledger.

## Stage 1 — Customer research
Use `customer-research`. Define customer groups, concrete jobs-to-be-done, operational pain, objections and customers' own language. Prioritize first-party research, interviews and actual case material; external research can indicate hypotheses but must not be presented as verified customer evidence. When no research exists, mark personas/needs as hypotheses rather than inventing interviews.
Deliver: audience map, prioritized problems, evidence confidence and outstanding research questions.

## Stage 2 — Offer and positioning
Use `offers`. For each *confirmed* service state who it serves, what is delivered, the process, conditions/limitations, and potential benefits in concrete terms. Avoid invented guarantees, savings percentages, client names, case studies, certifications or turnaround times. Specify one main CTA and a sensible low-friction secondary action if appropriate.
Deliver: offer map, value proposition, differentiation assumptions, proof requirements, CTA decision.

## Stage 3 — Page architecture and copy
Use `copywriting`. Develop a cohesive logical progression that answers: what do you do → what problem does it solve → how does it work → why trust you → what happens next? First draft section outlines; then draft headline, subtitle, brief explanatory copy, CTA and optional illustration caption per section. Prefer precise Russian language, modest length and human tone. Preserve good existing phrasing; don't fill arbitrary page length. Existing workflow diagrams and factual sequences should inform copy, not be redesigned to match a new slogan.
Deliver: `docs/CONTENT_STRATEGY.md` and `docs/WEBSITE_COPY.md` in project (or drafts for approval if explicitly requested).

## Stage 4 — Editing and claim verification
Use `copy-editing`. Eliminate AI clichés, buzzwords, false precision, repetitive wording, bureaucratic jargon, overly long paragraphs and unclear CTAs. Verify every factual claim against project evidence. Mark placeholders or questions rather than making up credentials, numbers or client names. Check readability on mobile, tone consistency, grammatical Russian and accessibility of labels.
Deliver: reviewed, concise copy and a list of claims requiring evidence.

## Stage 5 — Content → visual mapping
For each finalized section map: reader question → exact message → demonstrated real process → graphical entities → technically plausible transitions → optional scroll interaction → mobile/reduced-motion alternative. Produce `docs/CONTENT_VISUAL_MAP.md`. Don't lock in Three.js, shaders or visually expensive motion before identifying a genuine explanatory benefit.

## Handoff and gates
- If user requests content first, **do not edit implementation or trigger visual workflow**. Present draft content for approval, then hand off only after approval.
- When user authorizes an entire site build, pass completed or explicitly provisional copy into `workflows/landing-page.md` automatically, clearly reporting assumptions; no need to repeatedly ask permission.
- If factual uncertainty would materially change a claim, mark it and use a safe factual alternative.
- If content drafts already exist, improve them rather than replace their voice.
- Do not claim customer interviews, web evidence, user testing or conversion results without actually obtaining them.
