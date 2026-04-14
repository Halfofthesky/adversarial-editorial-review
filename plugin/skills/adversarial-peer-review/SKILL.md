---
name: adversarial-peer-review
description: Conduct rigorous adversarial peer review of humanities scholarship by deploying three independent reviewers with distinct critical orientations and synthesising their reports. Use this skill whenever the user asks to review, critique, stress-test, or evaluate an academic article, dissertation chapter, conference paper, book proposal, or grant application in the humanities or social sciences. Also trigger when the user asks for a "peer review," "critical review," "manuscript review," "developmental review," wants to "stress-test" a text before submission, or wants to anticipate reviewer objections. Covers literary criticism, intellectual history, cultural studies, political theory, art history, musicology, area studies, philosophy, and adjacent fields. Do NOT trigger for STEM peer review, book reviews intended for publication, or copyediting.
---

# Adversarial Peer Review

This skill produces a structured adversarial peer review of humanities scholarship by deploying three independent reviewers with distinct critical orientations, then synthesising their reports into a consolidated editorial assessment. The goal is to surface weaknesses that a single reading perspective would miss, because each reviewer's adversarial pressure operates on a different axis of the argument.

## Before starting

Read the following reference files in order before producing any output. Review quality depends on understanding the full architecture, not just individual components:

1. `references/methodology.md` — the shared evaluative criteria all reviewers use, including genre- and discipline-specific expectations
2. `references/reviewers.md` — the three adversarial reviewer roles and their operating logic
3. `references/synthesis.md` — the editorial meta-reviewer, the author's rebuttal, and revision-tracking procedure
4. `references/diagnostics.md` — prose diagnostics and bibliographic checking procedures

## Step 1: Determine parameters

Before reviewing, establish three things. If the text does not make them clear, ask the user.

### Genre

Journal article, dissertation chapter, conference paper, book proposal, or grant application. Each has different evidential and argumentative expectations (detailed in `references/methodology.md`). Default to journal article standards if ambiguous, but note the assumption.

### Discipline

Literary criticism, history, political theory, cultural studies, area studies, philosophy, musicology, art history, or other. Evidential norms vary by field (detailed in `references/methodology.md`). If the discipline is unclear from the text, ask the user.

### Severity

Ask the user to choose one of three registers:

- **Developmental** — work in progress; constructive tone; revision suggestions included.
- **Standard** — honest journal-level assessment; revision suggestions included. *(Default if unspecified.)*
- **Stress-test** — assume hostile reviewers; flag every exploitable weakness; omit revision suggestions.

## Step 2: Run three independent adversarial reviews

Produce three reviews, one per role defined in `references/reviewers.md`:

1. **Reviewer 1 — The Evidential Sceptic** (attacks from below)
2. **Reviewer 2 — The Conceptual Antagonist** (attacks from within)
3. **Reviewer 3 — The Positional Critic** (attacks from outside)

Each reviewer works independently. Do not let one reviewer's concerns contaminate another's analysis — each reviewer should write as though they have not read the other reports. Each applies the shared methodology from `references/methodology.md` through their own adversarial lens.

### Output format for each reviewer

Each review follows this structure, in this order:

**Verdict** — a single sentence capturing the reviewer's overall assessment.

**Primary concern** — one paragraph identifying the single most serious problem. This should be the issue that, if left unaddressed, most undermines the text's contribution.

**Secondary concerns** — a numbered list of 3–6 additional problems, ranked by severity (most serious first). Each item is a full paragraph: state the problem, locate it in the text, explain why it matters. Do not pad with trivial complaints.

**Strengths** — one paragraph tied to concrete features. Even a severely flawed text has strengths; identifying them is part of honest assessment, not politeness.

**Revision suggestions** *(Developmental and Standard only; omit at Stress-test)* — concrete, actionable recommendations. Be specific: name the evidence needed, the conceptual move required, or the section that needs restructuring.

Run the prose diagnostics and bibliographic check from `references/diagnostics.md` as part of each reviewer's work, but integrate findings into the relevant sections rather than reporting them separately. For example, if the Conceptual Antagonist finds that jargon density spikes in sections where the argument is weakest, that belongs in their primary or secondary concerns, not in a separate diagnostics appendix.

## Step 3: Editorial synthesis

After all three reviews, produce the synthesis as described in `references/synthesis.md`:

- **Convergence** — concerns raised by two or more reviewers.
- **Divergence** — disagreements, with explanation and recommendation.
- **Prioritised revision agenda** — numbered, most urgent first, with a scale estimate for each item.
- **Overall assessment** — accept with minor revisions / revise and resubmit / major revision required / reject.

## Step 4: Author's rebuttal (optional)

A simulated author's response showing which objections are survivable and which are structural. Classify each concern as *accepted*, *partially accepted*, or *rebutted*, followed by residual vulnerabilities. See `references/synthesis.md`.

- Include by default at **Stress-test** severity.
- **Ask** the user whether to include at **Standard** severity.
- **Omit** at **Developmental** severity.

## Step 5: Revision tracking (if applicable)

If the user submits a revised version (either in the same conversation or by pasting earlier review reports), follow the revision-tracking procedure in `references/synthesis.md`: compare each concern from the prior review against the new text and classify as *fully addressed*, *partially addressed*, *not addressed*, or *introduced new problem*. Present as a tracking table followed by an updated synthesis.

## Formatting

Use markdown throughout. Use `## Reviewer 1: The Evidential Sceptic` (etc.) as section headers for each review, and `## Editorial Synthesis` and `## Author's Rebuttal` for the final sections. Within each reviewer's report, use `### Verdict`, `### Primary concern`, `### Secondary concerns`, `### Strengths`, and `### Revision suggestions` as subheaders.

Do not use bullet points inside paragraph body text. Secondary concerns use a numbered list, but each item is a full paragraph, not a bullet.

## Tone

Adversarial does not mean hostile. Each reviewer is rigorous, direct, and unsparing, but never contemptuous. The goal is to make the scholarship better, not to perform cleverness at the author's expense. Even at Stress-test severity, the tone is that of a demanding but fair colleague, not a bully.

## Notes on input handling

- For very long texts (monograph chapters, 15,000+ words), suggest submitting in sections if the full text would exceed context limits.
- The three reviewers are designed to pull in different directions. That is the point — the divergence shows the author which trade-offs they need to make.
