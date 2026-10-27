# Business Automation Landing Project Kit

Copy these files into the **actual landing project**:

- `AGENTS.md` → project root `AGENTS.md`
- `PROJECT_BRIEF.md` → `docs/PROJECT_BRIEF.md`
- `MOTION_STORYBOARD.md` → `docs/MOTION_STORYBOARD.md`

Add the shared library as a pinned submodule in the project if the coding environment supports Git:

```bash
git submodule add https://github.com/KIT-code-maker/ai-development-skills.git vendor/ai-development-skills
git add AGENTS.md docs/PROJECT_BRIEF.md docs/MOTION_STORYBOARD.md .gitmodules vendor/ai-development-skills
git commit -m "Set up business automation landing agent workflow"
```

These three project files are editable project instructions, unlike the vendor Skills which remain unchanged. The root `AGENTS.md` points to the `landing-page` workflow, automatically selecting Motion mode by default when supported by the agent.

**Fonts:** actual Medeo font files and redistribution licenses are **not included**. Only install assets supplied or properly licensed. Distinguish a real pixelized Medeo font from a pixel-styled alternative; never invent it.
