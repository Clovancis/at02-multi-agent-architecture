[Version française](PERMISSIONS.fr.md)

# Permissions and mandate

## Principles

Least privilege, explicit scope, limited duration, separation of reading/proposing/executing, revocability, traceability, and no self-elevation.

## Levels

- **P0 Observe**: read the explicit scope without modification.
- **P1 Analyze**: produce analysis or proposals without persistent modification outside drafts.
- **P2 Prepare**: create a reversible artifact in a designated space.
- **P3 Execute after approval**: perform an external or persistent action after required authorization.
- **P4 Execute within a preauthorized framework**: perform a bounded, logged class of actions with a stop mechanism. P4 never authorizes changing the mandate itself.

Each permission states actor, action, target, purpose, duration, reversibility, control, and escalation.

A subagent receives an appropriate subset of capabilities. If the environment technically exposes more tools, the logical mandate remains narrower and compensating controls should prevent or detect out-of-scope use.

Operational autonomy permits choosing how to complete an authorized task. It does not permit changing the objective, broadening the target, obtaining new privileges, or disabling shutdown.

The real and immediate threat-to-life clause is not technical permission. A software agent may never invoke it to bypass a restriction, expand privileges, or resist an authorized shutdown.

## Deny by default and stopping

Deny by default applies to everything that extends an action or power: execution, privilege, scope, or duration. It may not make the brake unavailable. Each component may stop its own action in progress, even when the gateway state is ambiguous.

A global halt, interrupting several components or the system, is triggered by the principal, a designated safety component, or two independent components observing the same pre-written safety criterion. Two components are independent when they share neither the same working context nor the same intermediate reasoning chain and, where possible, rely on neither the same model nor the same provider. Independence is declared in the mandate and never presumed; two instances of the same model do not suffice to guarantee it. Its scope, maximum duration, and resumption procedure are defined in advance. A rollback is an action in its own right: it follows the applicable permissions and is never automatic when it may destroy data or effects.
