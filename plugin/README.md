# Adversarial Editorial Review — Cowork Plugin

A Claude Cowork plugin that produces structured adversarial peer review of humanities scholarship. Three independent reviewers with distinct critical orientations (Evidential Sceptic, Conceptual Antagonist, Positional Critic) read the submitted text, followed by an editorial synthesis and an optional author's rebuttal.

## What it gives you

- **Skill** — `adversarial-peer-review`, auto-triggered when you ask Claude to review, critique, or stress-test an academic text in the humanities or social sciences.
- **Command** — `/review`, an explicit trigger for the same workflow.

## Install

### From the `.plugin` file

Drop `adversarial-editorial-review.plugin` into a Cowork chat. A "Install plugin" button appears; click it.

### From source

Copy the `plugin/` directory into `~/.claude/plugins/adversarial-editorial-review/` (or the equivalent on your platform). The plugin.json manifest at `.claude-plugin/plugin.json` is the entry point.

## How to use

Start a new chat, attach or paste the text, and either:

- Ask naturally: *"Review this article."*, *"Stress-test this before I submit to Modern Language Review."*, *"Give me a developmental review of this dissertation chapter."*
- Or run the slash command: `/review`

Claude will ask for any missing parameters (genre, discipline, severity) and then produce the full review.

## Severity levels

- **Developmental** — constructive, for works in progress.
- **Standard** (default) — honest journal-level assessment.
- **Stress-test** — assumes hostile reviewers and flags every exploitable weakness.

## Scope

Covers literary criticism, intellectual history, cultural studies, political theory, art history, musicology, area studies, philosophy, and adjacent fields. Not designed for STEM peer review, book reviews intended for publication, or copyediting.

## Caveats

- For monograph-length chapters or texts over ~15,000 words, submit in sections.
- The three reviewers are designed to pull in different directions. Divergence between them is a feature, not a bug — it shows which trade-offs the author needs to make.

## License

MIT. See `LICENSE` at the repository root.
