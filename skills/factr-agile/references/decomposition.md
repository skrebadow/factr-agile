# Decomposition and allocation

Use for SPLIT capabilities. Choose the boundary that serves the requested outcome.

## Product slices versus system allocation

**Product decomposition** groups work around a useful capability, actor outcome, or coherent lifecycle. A slice should explain what becomes available and under which constraints. It need not map to one subsystem.

**System allocation** separates functional responsibility at architecture boundaries supported by supplied context. Distinct control, protection, approval, or reporting obligations may justify separate responsibilities. They do not establish component names, ownership, or implementation technologies by themselves.

If the user requests both, keep product grouping and technical ownership separate. Do not convert an unknown subsystem into a fictional confirmed team. For an underspecified request, use the interpretation supported by the input and label material allocation assumptions.

## Decide whether and where to split

- Already narrow, allocated scope may need refinement rather than further decomposition. Say why it is already appropriately bounded.
- Split independent responsibilities when one can hold while another fails; retain their dependencies and shared constraints.
- Do not split every verb, requirement, acceptance criterion, or implementation layer into a separate product item. A connected save-and-reopen capability can have several criteria within one story.
- Do not merge independent workflows merely because they share a noun, subsystem, setup, protocol, or release label.
- Do not impose a child count, hierarchy depth, or equal-sized slices.
- Retain exceptions and protective obligations. An approval clause does not silently authorize impacts otherwise prohibited by the source.
- Distinguish an enabling dependency from an established sequence. Do not invent ordering or cross-boundary guarantees.

For system requirements, a single declarative `shall` statement per child is useful when the source or requested format uses normative requirements. Label it as a candidate allocation unless accepted authority is supplied. For product slices, natural capability wording is appropriate.

## Source accounting

Use the full relevant source text available, not just IDs or grouping titles. Preserve exact quotations when quoting a parent; derived child wording can clarify meaning while preserving constraints.

For a finite selection, track which obligations each child retains, which apply to multiple children, which are not split further, and which remain unresolved or excluded. Duplicate input IDs need a source/revision distinction; report conflicting duplicates instead of silently overwriting them. A requirement linked to a child is not necessarily semantically covered.

When only an excerpt was supplied, scope completeness to that excerpt. Account for an explicit exclusion rather than dropping inconvenient obligations to make a grouping fit. If a behavior could belong to several supported boundaries, present alternatives or a provisional responsibility without claiming settled allocation.

## Useful output shape

Choose a table for parallel slices or a short section per child when details would make a table unwieldy. Retain as applicable:

- Child ID/title and capability or candidate requirement.
- Source reference and concrete obligations retained.
- Responsibility/owner, with explicit versus proposed support.
- Why this boundary is useful and any grounded dependency.
- Observable completion condition.
- Material open decisions, assumptions, and exclusions.

Keep source quotes outside a wide table if that improves readability. End with a scoped statement of what was allocated or grouped and what remains open. Do not claim downstream approval or generate tests, automation, or another product's artifacts merely because completion conditions are present.

## Illustrative boundary decision

Input: `R-1: Operators may restart Service A without interrupting Service B. Exceptions require a maintenance approver's authorization.`

Supported responsibilities include restart control, protection of Service B, and exception authorization. Architecture names for the mechanisms are unknown. If subsystem allocation is requested, describe those responsibilities and label ownership as proposed. Preserve the uncertainty about what an exception authorizes: permission to restart, permission to interrupt B, or another bounded action. Do not silently delete the continuity constraint or choose the broadest permission.

If product shaping is also requested, connect the responsibilities only to the extent that the source establishes one maintenance capability. Keep the operator and maintenance approver's distinct authorities visible.
