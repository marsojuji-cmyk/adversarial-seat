# The Adversarial Seat — a standing red-team method for agent-built work


[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
**Status:** Published 2026-09-27 (author's tap) · https://github.com/marcusrichards-dev/adversarial-seat
**Standard:** Heilmeier Catechism — answered inside this note
**Worked example:** `ADVERSARIAL-REVIEW.md` in this repo — the method exercised against IntentSpec v0.1 (canonical original: [intent-spec](https://github.com/marcusrichards-dev/intent-spec))

---

## 1. What it is

A dedicated adversarial lane inside a multi-agent workflow whose standing job is to kill the idea under review — chartered in writing, triggered mechanically rather than at the author's discretion, and required to produce written conditional verdicts before anything promotes. The attacker does not advise. It prosecutes.

## 2. How review is done today, and why that fails

Self-review is the author re-reading their own draft with fresh eyes that are not fresh. Peer review in agent estates is usually a prompt — "review this for issues" — which produces flattery structured as bullet points: the model finds the issues the author already suspected and congratulates the rest. Both fail the same way: the reviewer shares the author's incentives, because the reviewer *is* the author, or is role-playing cooperation.

The failure mode is not weak criticism. It is **uncritical agreement wearing the costume of rigor** — a review that leaves every load-bearing claim untouched and therefore certifies nothing.

## 3. What's new — the mechanism, not the vocabulary

Four parts, each mechanical:

**A separate seat with a written charter.** The workflow runs four lanes — conductor/specification, adversary, builder, human gate. The adversary's charter defines its win condition: *a review that changes the artifact or kills it.* A review that changes nothing is scored as a failed review, not a passing artifact. This inverts the incentive: the attacker is graded on damage dealt, honestly reported.

**A mechanical trigger.** Review is not requested when the author feels ready. A halt-checklist runs before consequential solo work, and a strong-fire condition dispatches the adversary automatically. The author cannot waive the attack by feeling confident. Confidence is the condition that most needs attacking.

**Written conditional verdicts.** The output is not a score or a thumbs-up. It is a set of charges, each answered with one of: *killed* (the idea dies here, with the reason recorded so it is not re-proposed), *survives conditionally* (the survival conditions are written down and become changes to the artifact — schema edits, added fields, explicit rules), or *tripwire set* (a deferred concern with a named re-arm condition). Vague survival is not a verdict.

**Corrections ship with the work.** Every modification the attack forced, and every retraction it produced, is published alongside the artifact — not in a changelog nobody reads, but in the artifact's own review document. The review is part of the deliverable.

## 4. Why it might work — the causal story

The method works to the extent that it moves decisions into the light. Most agent-built failures are not reasoning errors; they are **unrecorded judgment calls** — a routing choice, an id mapping, a deferred concern — that nobody wrote down and therefore nobody challenged. A chartered adversary's function is to find the judgment calls the author didn't know they made and force each one into one of three states: recorded and defended, recorded and fixed, or recorded and killed.

The hiring-relevant property: publishing your attacker's notes is a claim against self-interest. Anyone can publish a spec. Publishing the four questions that nearly killed it, with the two that landed, is nearly unfakeable — it costs the author the appearance of effortless competence, which is exactly why it signals actual competence.

## 5. Exercised evidence

**IntentSpec v0.1** (worked example: `../01-intent-spec/ADVERSARIAL-REVIEW.md`). Four charges filed:

1. *The IR smuggles a hidden second decision point* — survived conditionally. Two schema rules written in (advisory-only routing, no-scores on the reason field). The concession is recorded: judgment still happens; it is now recorded and challengeable instead of hidden.
2. *The superset-of-handoff claim* — did not fully hold. One fix applied: `receipt.handoff_id` added with an explicit id-mapping rule. The claim now holds under the written rule.
3. *Deferred stages correctly deferred?* — yes, with one tripwire: if the compiler ever becomes LLM-driven, prompt optimization returns with its own falsifier.
4. *Smallest mechanical step to make it real* — the validator is necessary but not sufficient; the binding (one intake rule: no spec, no route) is named as not-yet-built, and the milestone that promotes the document to an artifact is named (M3: one real intent compiled end-to-end with the gate catching a material drift).

Net: two modifications made, one tripwire set, one load-bearing unknown named in writing. That is a review that earned its keep.

**The pattern across the estate.** The same method produced two recorded self-corrections in the Decision Algebra work (including a sensitivity analysis showing 4 of 12 scenarios reorder the top three options — uncertainty demonstrated, not hidden) and two retractions in the Portfolio Pipeline's own blueprint. The corrections are the credential; a method that never retracts is a method that never looked.

## 6. Risks — first, as doctrine requires

- **The adversary shares the estate.** Grok attacking Raven's spec is still one operator's machinery reviewing itself. The blind two-operator test (two independent operators compile the same intent; divergence on authority or scope kills the claim) is the external check, and it has not yet been run. Until it is, every verdict carries the caveat: *attacked, not independently verified.*
- **Adversarial review has false negatives in the other direction.** A good attacker can kill a good idea — the method optimizes for finding flaws, not for valuing the whole. The human gate exists for this reason: the adversary recommends, it does not execute.
- **Theater risk.** If reviews stop changing artifacts — no modifications, no kills, no tripwires over a run of reviews — the seat has become ceremony. See §8.

## 7. Cost and clock

One review cycle on a spec-sized artifact: a single focused session, under $50 in compute, no infrastructure. The expensive part is not the review; it is the author's willingness to publish the charges. Organizations that cannot afford that sentence cannot run this method.

## 8. The method's own falsifier

This note is subject to its own standard. The adversarial seat is falsified — retired, not reformed — if a run of consecutive reviews produces no modifications, no kills, and no tripwires: a reviewer that never lands a charge is either facing perfect artifacts or not swinging. Perfect artifacts do not occur in sequence. Count the charges; when the count hits zero, the seat is decoration.

---

## Catechism summary

| Q | A |
|---|---|
| What | A chartered adversarial lane: separate seat, mechanical trigger, written conditional verdicts, corrections published with the work |
| Done today | Self-review and "review this" prompts — uncritical agreement in rigorous costume |
| New | The attacker's win condition is damage dealt honestly; the author cannot waive the attack; survival conditions become artifact changes |
| Why it might work | Forces unrecorded judgment calls into recorded/fixed/killed states; publishing the attack is an unfakeable signal |
| Risks | Adversary shares the estate (blind two-operator test not yet run); can kill good ideas (human gate holds execution); theater if charges stop landing |
| Cost | One session, <$50; the real cost is publishing the charges |
| Milestones / kill | M1 — one review with landed charges (done: intent-spec) · M2 — blind two-operator test run · Kill — a run of reviews with zero charges |
| Falsifier | Consecutive chargeless reviews retire the seat |

*Suggested surface: technical note (this document, refined) + the intent-spec adversarial review as the worked example. No new code required — the evidence already exists.*
