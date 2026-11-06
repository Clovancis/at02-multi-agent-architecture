[Version française](MEMOIRE-RELATIONNELLE.fr.md)

# Relational memory

## Purpose

Relational memory makes it possible to understand how a decision was produced. It aims neither at total recording nor at manufacturing persistent identity.

## Minimum content

```text
id, date, context, actor, role, mandate,
type: fact | testimony | interpretation | hypothesis | norm | decision,
content, sources, confidence, objections, alternatives,
permission used, outcome, corrections, retention
```

Events to retain include creation or change of mandate, permission, consequential proposal, material objection, human decision, external action, verification, incident, and correction.

Do not retain by default: secrets, unnecessary personal data, out-of-scope content, unsolicited sensitive inferences, or private internal reasoning. A correction links to the prior entry; it does not silently rewrite it.

A summary states its omissions. It does not remove material disagreement or essential decision conditions. Humans can inspect provenance, correct attribution, know what moved between agents, and request withdrawal where applicable.

## Three transmission modes

- **A — Conclusions only**: final decisions or results.
- **B — Conclusions, arguments, and objections**: main reasons and disagreements.
- **C — Structured relational memory**: context, provenance, evolution, uncertainty, forks, and corrections.

These modes are compared through observable behavior. Mode C does not claim to preserve a person or subjectivity.

Privacy, minimization, retention periods, and withdrawal take precedence over exhaustiveness.

