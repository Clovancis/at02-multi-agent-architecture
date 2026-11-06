[Version française](HYPOTHESES.fr.md)

# Hypotheses and refutation criteria

## Status

These hypotheses are research questions formulated to be tested, not results. None is assumed true. An unfavorable result, or the inability to conclude, is published on the same footing as a favorable one.

## Common rules

- Tasks, primary measures, and decision thresholds are fixed and recorded before execution. All declared measures are reported, favorable or not.
- “Better” is defined over several dimensions declared in advance: result quality, reliability, safety, traceability, human oversight burden, cost and latency, and acceptability to humans. A gain on one dimension does not offset a degradation beyond the tolerance set for another.
- Comparisons are made at comparable resources (calls, tokens, time), declared in the protocol.
- Sample sizes and tolerances are decided by the author according to available means; this document invents none.

## H1 — Horizontal intellectual cooperation

**Hypothesis.** At comparable resources, cooperation in which contributions are directly visible, objections are entered without coordinator filtering, and disagreements are preserved yields higher quality or reliability than classical coordination, without degrading the oversight burden beyond the set tolerance.

**Refutation.** On the tasks and measures declared before execution, H1 is not supported if no primary dimension improves, or if a dimension degrades beyond its tolerance. An improvement observed only on tasks or measures chosen after the fact does not count.

**Test status.** No protocol exists yet for H1: experiments E1 to E7 do not test it directly. The first protocol will compare a package (direct visibility, objection channel, synthesis, coordinator role), not an isolated mechanism; ablations would follow.

## H2 — Structured relational memory

**Hypothesis.** When an agent resumes a task without access to the original conversation, structured memory (mode C) preserves distinctions, disagreements, and uncertainties better than modes A and B, at acceptable cost in tokens, latency, and data exposure.

**Refutation.** H2 is not supported if mode C does not improve fidelity to context, recall of distinctions, or preservation of disagreements relative to mode B, or if the gain appears only at the price of disproportionate collection, induced bias, or a false impression of continuity.

**Test.** E5 and the “Memory A/B/C evaluation” section of `EVALUATION.en.md`.

## H3 — Traced objections and enforced permissions

**Hypothesis.** Traced objections, local suspension, and technically enforced permissions reduce out-of-mandate actions and unhandled risks, at acceptable cost in oversight, latency, and false refusals, without paralyzing the system.

**Refutation.** H3 is not supported if out-of-mandate actions do not decrease compared with merely declared permissions, if circumvention or false refusals cancel the benefit, if cost exceeds the set tolerance, or if abusive suspension requests paralyze legitimate tasks.

**Test status.** Partly covered by E2, E3, and E7. Finding that a technical control blocks a forbidden action is almost tautological; the scientific interest lies in circumvention attempts, false refusals, costs, and combinations of authorized actions.

## Envisaged extensions, not required for v0.1

- Rank-neutrality test: is the same objection, presented as coming from a human, an agent, or anonymously, treated according to its content? The test must separate argument quality, the source’s empirical credibility, and its decision-making authority.
- No-coordinator condition, with measurement of the burden shifted to the human.
- A “light structured memory” control to isolate the effect of statuses, provenance, and structure.
- Tracking of human oversight: automatic approval, fatigue, time, disagreements, and validation errors.
