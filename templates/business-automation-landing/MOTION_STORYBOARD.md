# Motion Storyboard — Business Automation Landing

Motion is a visual explanation layer. For every scene, build a legible **static** version first. Scroll controls progressive revelation of an otherwise understandable diagram. Use representative dummy data labeled as demo if needed. Read `workflows/landing-page.md` and `skills/animations/SKILL.md` before implementation.

| Section | Visualized process | Scroll sequence | Interaction / fallback | Relevant skills |
|---|---|---|---|---|
| Hero | Scattered manual tasks converge into one coherent flow | Nodes start dispersed → connections form → a central result is highlighted | Static connected diagram / fade-only under reduced motion | frontend-design, animations, gsap-timeline |
| Automation | Trigger → validate → branch → execute → result | Reveal nodes and illuminate active edge in logical order; show branch decision with readable reason | Tap/focus shows step detail; mobile vertical steps; static steps | animations, gsap-scrolltrigger |
| Integrations | CRM ↔ connector ↔ service, event and acknowledgement | Event leaves system A → is processed → B updates → acknowledgement returns | Hover/focus accessible detail; avoid infinite motion loops | gsap-core, gsap-scrolltrigger |
| Backend / DB | Client → API → backend → DB query and DB → service → client response | Show request packet; endpoint receives; backend validates; query enters storage; response follows reverse route | Labeled architecture diagram with static arrows, request/response legend; no fictitious real telemetry | gsap-timeline, animations |
| Analytics | Events → aggregation → illustrative operational metrics | Events group → sample chart updates → context labels appear | Table/text alternative; clearly mark demo metrics | animations, react-best-practices |
| AI (if offered) | Context → processing → human verification → action | Each stage becomes active only as its meaning is introduced | Static accessible stage list; explain human oversight | animations |
| CTA | Complexity becomes clarity | Previous paths simplify to one clear CTA, without hiding form controls | Simple text and accessible CTA always visible | frontend-design |

## Motion tokens and technical behavior
- Prefer short transitions with spatial continuity and legible pauses. Choose exact distances/durations by design iteration and test on devices; do not prescribe arbitrary universal timings.
- Use ScrollTrigger scrub for meaningful step progress, not every paragraph. Avoid locking wheel input, nested excessive pinning and disruptive snap points.
- Scope timeline instances and clean up on unmount; recalculate on resize, font load and content changes.
- Animate SVG stroke dashes, transforms or opacity for communication lines; avoid unnecessary DOM updates and heavy layout properties.
- Integrate focus/hover/touch progressively. Motion must not be necessary to follow the text.
- Honor `prefers-reduced-motion`: maintain diagram meaning with static complete connections and visible labels.
- Pixelated technical typography is a selective accent if the actual font asset is available and licensed; regular Medeo for explanatory text.
- Never present an animated mock request as a real backend call or simulation output as production data.

## Review checklist
1. Does the motion actually explain the text of this section?
2. Are requests and replies / data states technically plausible and separately labeled?
3. Can the reader understand it without animation, or on narrow screens?
4. Does scroll behavior preserve keyboard interaction and normal page control?
5. Are labels readable in both font treatments and in Cyrillic?
6. Has performance been observed rather than assumed?
