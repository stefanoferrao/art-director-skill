# art-director-skill

An **Art Director + Director of Photography** skill for AI coding agents (Claude Code, Codex, Cursor and any agent that reads `SKILL.md`). It directs and reviews the visuals of games, cutscenes and real-time 3D: framing, camera moves, lenses (dolly zoom, DOF, bokeh), light, palette, and a strict self-critique loop with an independent critic.

Engine-agnostic: Unity, Unreal, Godot, Blender, three.js.

[Leia em português](README.pt-BR.md)

## What it does
- Reads your project's style bible (`ART_DIRECTION.md`) first and treats it as law. No bible yet? It offers to write one from the included template.
- Describes each shot in one sentence: lens, movement, framing, light.
- Runs a camera pipeline: beats, baseline stills, 2–3 coverage options, implement, then an **independent critic** (another model, read-only, 1–5 per shot plus "the five fixes that matter"), then fixes. About 5 rounds.
- Reviews strictly against your references and reports each finding as file/scene, problem, fix.
- Plans first, then asks: Continue / Change / Add / Plan only.

## Install

**Claude Code (all projects):**
```bash
git clone https://github.com/stefanoferrao/art-director-skill.git
mkdir -p ~/.claude/skills
cp -r art-director-skill/art-director ~/.claude/skills/
```

**Claude Code (one project only):** copy `art-director/` into `<your-repo>/.claude/skills/`.

**Other agents:** copy `art-director/` into the skills folder your agent reads. Or point the agent at `art-director/SKILL.md` as an instruction file.

Then write `@art` or ask things like "review this cutscene's camera" or "why does this scene look amateur?".

## Customize
Put your look in `ART_DIRECTION.md` at the root of your project (start from `art-director/templates/ART_DIRECTION.md`). The skill stays generic; your project file decides palette, light and limits.

## License
MIT
