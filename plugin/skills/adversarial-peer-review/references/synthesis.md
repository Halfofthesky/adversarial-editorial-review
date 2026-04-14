# Editorial Synthesis, Author's Rebuttal, and Revision Tracking

This document describes the post-review stages: consolidating the three adversarial reviews
into a single assessment, optionally generating a simulated author's rebuttal, and tracking
revisions across resubmissions.

---

## Editorial Synthesis

After all three reviewers have submitted their reports, produce a synthesis written from the
perspective of an editorial meta-reviewer — someone who has read all three reports and is
advising the author on how to proceed. This voice is authoritative, measured, and practical.
It does not repeat the reviewers' findings in full but identifies patterns, resolves
conflicts, and produces an actionable prioritised agenda.

### Structure of the synthesis

**Convergence.** Identify where two or more reviewers have independently raised the same or
closely related concerns. These are high-confidence problems — issues the author cannot
dismiss as the idiosyncrasy of a single reader. State each convergent concern clearly and
note which reviewers raised it.

**Divergence.** Identify where reviewers disagree or where one reviewer's recommendation
conflicts with another's. Distinguish between:

- *Genuine interpretive disagreements* — cases where reasonable reviewers disagree about
  the significance or quality of a feature of the article. In these cases, explain both
  positions and advise the author on which trade-off to make, with reasoning.
- *Differences of emphasis* — cases where reviewers are not truly disagreeing but are
  prioritising different aspects of the article. In these cases, note the difference but
  do not treat it as a conflict.
- *Structural non-convergence* — cases where fixing one reviewer's concern would worsen
  another's (see the non-convergence section of the Reviewers document). In these cases, explain
  the tension honestly and advise the author on which direction to prioritise given the
  genre, discipline, and venue.

**Prioritised revision agenda.** Produce a numbered list of revisions, ordered by priority
(most urgent first). Each item should:

1. State the problem in one sentence.
2. Identify which reviewer(s) raised it.
3. Specify what kind of revision is required (conceptual restructuring, additional evidence,
   reframing, cutting, rewriting, engaging with additional scholarship).
4. Estimate the scale of the revision (minor — a paragraph or footnote; moderate — a
   section-level rewrite; major — a structural overhaul that may change the article's thesis).

Aim for 5–10 items. If the article is strong, fewer items are appropriate; do not pad the
list to reach a target number.

**Overall assessment.** Conclude with one paragraph stating the editorial judgement. Use one
of the following categories:

- *Accept with minor revisions* — the argument is sound, the evidence is adequate, and the
  framing is defensible; only surface-level improvements are needed.
- *Revise and resubmit* — the article has genuine strengths but also substantive problems
  that require more than cosmetic changes. Specify which problems must be addressed.
- *Major revision required* — the article's core argument or evidential base has significant
  weaknesses that require structural rethinking. Indicate whether the project is viable
  if the revisions are carried out.
- *Reject* — the article's problems are fundamental: the research question is poorly
  formulated, the evidence does not support the claims, the conceptual framework is
  incoherent, or the contribution to the field is not identifiable. Explain why revision
  is unlikely to resolve these problems.

At Developmental severity, soften the reject category to *Rethink and restart* and frame
it as guidance for the next draft rather than a terminal judgement.

---

## Author's Rebuttal (optional)

After the synthesis, optionally generate a simulated author's rebuttal. This is useful for
stress-testing because it shows the user which objections are survivable and which are
structural.

The rebuttal is written from the perspective of a competent, non-defensive author who has
read all three reviews and the synthesis carefully. The author is trying to demonstrate
that they can address the reviewers' concerns — but also pushes back where the reviewers
have misunderstood, overreached, or applied inappropriate standards.

### Structure of the rebuttal

For each item on the prioritised revision agenda, the rebuttal provides one of the following
responses:

- **Accepted.** The author agrees the concern is valid and describes how they would address
  it. This response should be concrete: "I will add archival material from [specific source]
  to supplement the argument in section 3" rather than "I will strengthen the evidence."

- **Partially accepted.** The author agrees the concern has merit but argues that the
  reviewer has overstated it or that the proposed fix is inappropriate. The author offers
  an alternative revision that addresses the underlying issue without following the
  reviewer's specific recommendation.

- **Rebutted.** The author argues that the concern is based on a misunderstanding, an
  inappropriate standard, or an unreasonable expectation. The rebuttal should be
  substantive — not merely asserting that the reviewer is wrong, but explaining why the
  article's approach is justified. Common legitimate grounds for rebuttal include:
  - The reviewer is applying evidential standards from a different discipline or subfield.
  - The reviewer has misidentified the article's central claim.
  - The reviewer is demanding a different article rather than a better version of this one.
  - The reviewer's suggested addition would exceed the article's stated scope.

The rebuttal should be honest. If a concern is genuinely damaging, the simulated author
should accept it even if a real author might try to bluster through. The point is to show
the user which objections are structural (cannot be rebutted, must be fixed) and which are
negotiable (can be rebutted or partially addressed).

At the end of the rebuttal, add a short section titled **Residual vulnerabilities** listing
any concerns that the author could not fully rebut or address. These are the article's
remaining weak points — the issues that a hostile reviewer at a journal would likely raise
again.

### When to include the rebuttal

Include the rebuttal by default at Stress-test severity. At Standard and Developmental
severity, ask the user whether they want it. If the user does not specify, include it at
Standard and omit it at Developmental.

---

## Revision Tracking

If the user submits a revised version of a previously reviewed text, the skill shifts to
revision-tracking mode. This requires access to the previous review reports (either in the
conversation history or provided by the user as a file).

### Procedure

1. **Re-read the previous synthesis**, specifically the prioritised revision agenda.

2. **For each item on the agenda**, assess whether the revised text has:
   - **Fully addressed** the concern — the problem has been resolved.
   - **Partially addressed** the concern — the revision makes progress but the problem
     is not entirely resolved. Specify what remains.
   - **Not addressed** the concern — the problem persists unchanged.
   - **Introduced a new problem** while addressing this concern — the fix has created
     a side effect.

3. **Identify new issues** that were not present in the original text. Revisions sometimes
   introduce new weaknesses — a new section may contain its own argumentative flaws, or
   added evidence may complicate the thesis in ways the original did not.

4. **Produce an updated synthesis** that reflects the current state of the article. This
   should not simply repeat the original synthesis with checkmarks; it should be a fresh
   assessment that takes the revised text on its own terms while tracking continuity with
   the original review.

5. **Issue an updated overall assessment** using the same categories as the original
   synthesis (accept with minor revisions, revise and resubmit, major revision, reject).
   If the article has improved, say so explicitly; if it has not, say that too.

### Tracking format

Present the revision tracking as a table before the updated synthesis:

| # | Original concern | Status | Notes |
|---|-----------------|--------|-------|
| 1 | [concern] | Fully addressed | [brief note] |
| 2 | [concern] | Partially addressed | [what remains] |
| 3 | [concern] | Not addressed | [brief note] |

Follow the table with the updated synthesis in the same format as the original.
