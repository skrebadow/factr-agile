# Backlog refinement

Use for SHAPE capabilities. Refine the requested abstraction level without generating unrequested parents or children.

## Select the useful level

- **Epic:** a broad capability or lifecycle with a grounded purpose and several meaningful slices.
- **Feature:** a cohesive capability with concrete boundaries and observable completion conditions.
- **User Story:** a narrow actor/outcome slice when the source grounds that relationship.
- **Acceptance criteria:** independently challengeable commitments belonging to the requested item or supplied scope.

Use a direct system-capability statement when meaningful behavior is supported but a human actor or distinct value is not. Do not force `As a / I want / So that` with a guessed role or tautological purpose. If a specific actor-value story is essential to the user's request and cannot be grounded, provide the common supported behavior and identify the decision needed.

An operator initiating a change and an approver authorizing an exception have distinct responsibilities. They may warrant separate stories within a feature, but do not require a new story for every atomic criterion.

## Add engineering meaning without invention

Extract actors/authority, triggers, relevant state, behavior, objects, concrete rules and thresholds, exceptions, and outcomes. Explain supported interactions or boundaries instead of repeating a requirement across title, rationale, contract, and success fields.

Preserve concrete details in the narrative and criteria. If removing IDs and a supplementary constraint table would make the artifact generic, improve the prose. Do not replace known values with `source-defined`, `applicable`, or `works correctly`. A source ledger may aid a large batch, but cannot carry meaning absent from the backlog item.

A grounded consequence may clarify purpose; a plausible business benefit remains inferred or proposed. Sparse input may only justify a concise capability statement and open decisions. Do not fabricate a rationale to make the output appear refined.

## Acceptance criteria as behavioral commitments

For each criterion make the responsible subject, relevant condition, one commitment, and observable outcome recoverable. Consider what contrary observation would contradict it. Express that distinction in the criterion or a concise failure note when helpful, rather than demanding a FACT table.

For example, given `R-12: Only administrators may change retention from 7 to 30 days inclusive; rejected updates leave the saved value unchanged`, preserve separate commitments:

- An administrator's accepted update sets the saved retention to the submitted supported value.
- A non-administrator's update is rejected.
- An update outside the inclusive 7–30 day range is rejected.
- After a rejected update, the saved retention is unchanged.

The rejection and unchanged-state commitments are independently challengeable. Do not add a particular API response, audit record, input syntax, or asynchronous timing guarantee not established by the source. If validation of non-integer values is unspecified, retain that unknown instead of assuming an integer-only rule.

Keep criteria at the product or responsibility boundary. Detailed setup sequences, test fixtures, Gherkin, selectors, and execution claims are not default Agile outputs. An observable acceptance condition is an expected behavior, not evidence of implementation.

## Handle material unknowns

When `retain settings` could mean preserving stored configuration or preserving effective behavior, keep those interpretations distinct. Deliver common supported scope or explicitly labeled alternatives when useful. Do not choose one and attach the unresolved question as if the choice were settled.

Preserve known constraints in each affected alternative. Keep secondary questions near their scope. Ask about product behavior or responsibility, not which FACTR artifact the user must provide. Reuse decisions already supplied.

## Presentation and traceability

Follow an existing requested template when it helps. Otherwise include the fields that add meaning:

- A useful title and capability/story statement.
- Grounded purpose when known.
- Scope and concrete rules.
- Observable acceptance conditions or epic-level success indicators.
- Sources and support labels.
- Material assumptions, dependencies, and open decisions.

Use local IDs when references across a batch require them; retain real requirement IDs exactly. List excludes/unresolved scope separately before claiming coverage. Preserve labels and material bases in saved artifacts. For repeated refinement, identify affected items and changed criteria without silently altering a supplied accepted baseline.

A release or sprint label may identify scheduling scope, but it is not the actor, capability, or acceptance outcome.
