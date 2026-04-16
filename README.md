# Adversarial Editorial Review

Rigorous adversarial review of humanities scholarship, delivered as a Claude skill.

Three independent reviewers with distinct critical orientations read the submitted text; an editorial synthesis consolidates their reports into a prioritised revision agenda and overall verdict. Designed to surface weaknesses that any single reading perspective would miss.

## What's in this repo

| Path | For whom | What it is |
|---|---|---|
| `skill/adversarial-peer-review/` | Claude Code, Cowork skill installers | A standalone skill folder with `SKILL.md` + `references/` |
| `plugin/` | Cowork plugin users | A Cowork plugin that bundles the skill plus a `/review` slash command |
| `dist/adversarial-peer-review.skill` | Everyone | Pre-zipped skill, ready to drop into Cowork |
| `dist/adversarial-editorial-review.plugin` | Cowork users | Pre-zipped plugin, ready to install in Cowork |

## Install

### Cowork (easiest)

Download `dist/adversarial-editorial-review.plugin` and drop it into a Cowork chat. Click the "Install plugin" button that appears. Or, if you only want the bare skill, use `dist/adversarial-peer-review.skill` the same way.

### Claude Code

Copy `skill/adversarial-peer-review/` into one of:

- Project-level: `.claude/skills/adversarial-peer-review/` (inside the repo you're working in)
- User-level: `~/.claude/skills/adversarial-peer-review/` on macOS/Linux, or `%USERPROFILE%\.claude\skills\adversarial-peer-review\` on Windows

Claude Code auto-discovers skills at those paths.

### claude.ai Projects

The skill format isn't directly compatible with the claude.ai Projects UI. If you want to run this inside a Project instead, create a Project, paste the contents of `skill/adversarial-peer-review/SKILL.md` into the Project Instructions, and upload the four reference files under Project Knowledge.

## Usage

Attach or paste the text, then ask naturally. The skill also responds to the `/review` slash command when installed as a plugin.

- *"Review this article."*
- *"Stress-test this before I submit to Modern Language Review."*
- *"Give me a developmental review of this dissertation chapter."*
- *"This is a revised version — compare against the previous review."*

Claude asks for missing parameters (genre, discipline, severity), then produces three independent reviews, an editorial synthesis, and — at Stress-test severity — a simulated author's rebuttal.

## Severity levels

- **Developmental** — constructive, forward-looking; for works in progress.
- **Standard** (default) — honest, journal-level assessment.
- **Stress-test** — assume hostile reviewers and flag every exploitable weakness.

## Scope

Covers literary criticism, intellectual history, cultural studies, political theory, art history, musicology, area studies, philosophy, and adjacent fields. Not designed for STEM peer review, book reviews intended for publication, or copyediting.

## A note on the name

The repo and plugin are named `adversarial-editorial-review`, but the skill inside them is `adversarial-peer-review` — because what the workflow simulates is peer review, performed by three adversarial readers. The "editorial" framing refers to the synthesis layer that reconciles their reports.

## Contributing

Issues and pull requests welcome. For substantive changes to the reviewer roles or methodology, open an issue first to discuss.

## License

MIT. See `LICENSE`.
