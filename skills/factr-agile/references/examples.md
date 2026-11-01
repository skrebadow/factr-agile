# Constructed Agile examples

These examples illustrate decisions. They are not requirements or observed software results.

## Direct story with incomplete persistence scope

Request: `Turn this into a story: Operators save notification preferences and see them when reopening settings.`

A grounded capability is saving and recalling an operator's preferences. Do not invent a productivity benefit for the story's `So that` clause. Use a concise capability statement if the input does not establish distinct value.

Possible acceptance conditions:
- After the operator saves supported values, those values are retained.
- When that operator reopens settings, displayed values match those saved.

These are two commitments within one cohesive item, not necessarily two stories. Keep support explicit in the supplied description. Sign-out, server restart, and another device are unknown persistence scopes, not required scenarios. No decomposition artifact or runtime evidence is needed to draft the item.

## Known permissions and numeric boundary

Request: `Shape R-12: Only administrators may change retention from 7 to 30 days inclusive. A rejected update leaves the saved value unchanged.`

Keep the administrator's authority, inclusive bounds, rejection behavior, and unchanged saved state visible in prose and criteria. Non-administrator rejection and unchanged state are different commitments. Do not invent an HTTP code, audit log, integer-only input rule, or approval workflow.

The source supports a controlled retention-setting capability. It does not establish a storage architecture or measured execution result.

## Allocation without architecture names

Request: `Split R-20: Restart Service A without interrupting Service B; exceptions require maintenance authorization. We have no architecture diagram.`

Propose responsibility boundaries for restarting A, maintaining B's continuity, and exception authorization, with ownership explicitly unresolved. Preserve the question of what an exception permits. Do not name fabricated subsystems or claim complete settled allocation while exception semantics remain unresolved.

## Multiple actors, cohesive feature

Request: `Create a feature and stories. Operators submit access requests. Security approvers approve or reject them. Requesters see the recorded decision.`

A request-and-decision feature can preserve submission, authorized disposition, and visibility. Use separate stories where different responsibilities and valuable outcomes warrant them. Do not assume operators and requesters are the same role unless supported. Preserve an unknown identity relationship; do not invent states, notification channels, or a decision deadline.

## Conflicting retention meanings

Request: `Refine “the service retains message priority.” This could mean stored path configuration or the priority of delivered messages; we have not decided.`

Present two labeled candidate feature interpretations and any common supported scope. Stored configuration and delivered-message behavior are different outcomes. Do not silently select one, infer delivery order from priority, or state a resolved acceptance criterion for an unresolved meaning.
