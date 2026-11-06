[Version française](ARCHITECTURE.fr.md)

# Relational architecture

## Objective

The architecture explicitly represents who acts, in what role, under which mandate, with what permissions, and with what avenue for challenge. It complements Harness controls; it does not replace them.

## Roles

- **Human principal**: sets the objective, limits, and reserved decisions.
- **Coordinator**: decomposes, delegates, and synthesizes without expanding the mandate.
- **Subagent**: performs a bounded task with authorized tools.
- **Reviewer**: examines a proposal using explicit criteria.
- **Memory steward**: preserves authorized decisions, objections, and corrections.
- **Environment**: resources, tools, and constraints in which actions occur.

A component may hold several roles; each decision records the active role.

## Objects

- **Mandate**: objective, scope, permitted and prohibited actions, reserved decisions, duration, and stop conditions.
- **Proposal**: an unexecuted action with rationale, uncertainty, alternatives, and reversibility.
- **Permission**: a technical capability granted by an identified authority for limited scope and time.
- **Objection**: structured disagreement classified as blocking or non-blocking.
- **Decision**: a choice attributed to an authority, with revision conditions.
- **Trace**: a versioned event corrected by addition, not silent rewriting.

## Cycle

1. The principal sets the mandate.
2. The coordinator proposes proportionate decomposition.
3. Required permissions are compared with available permissions.
4. Authorized tasks are executed or delegated.
5. Results state sources, uncertainty, and limits.
6. Relevant objections are examined for a limited number of cycles.
7. A determinative objection blocks or escalates; others are preserved.
8. A decision beyond mandate or with significant consequences goes to a human.
9. The authorized action is executed, verified, and traced.
10. New evidence may trigger revision.

## Invariants

- No agent expands its mandate or privileges.
- Operational autonomy exists only within the mandate.
- A synthesis does not erase material disagreement.
- An irreversible or consequential action requires the designated authority.
- Absence of agent objection is not human consent.
- Analysis depth is proportionate to consequences, uncertainty, and reversibility.

## States

```text
proposed -> reviewed -> authorized -> executed -> verified -> closed
                 \-> rejected
                 \-> revise
reviewed -> escalated -> human decision
executed -> challenged -> corrected or upheld
```

