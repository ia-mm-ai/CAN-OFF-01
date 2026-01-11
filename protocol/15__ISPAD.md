ISPAD - Irreversible & Safety-Scoped Action Dispatch Protocol

Status: CANONICAL
Class: Execution Legitimacy + Audit
Authority: BOUND (via PROPORTION + IAM.MAI where applicable)
Execution Power: LIMITED (authorize execution only)
Truth Power: NONE
Identity Power: NONE
Mutation Rule: Additive-only (via EVOLVE + CANON)

⸻

0. Canonical Statement

ISPAD governs whether an EXECUTION_REQUEST may be executed and how that execution is recorded without becoming truth, identity, or retroactive authority.

ISPAD:
	•	validates preconditions,
	•	enforces authority binding,
	•	requires human invocation where mandated,
	•	produces an EXECUTION_RECORD as an audit trace.

ISPAD does not decide policy.
ISPAD legitimizes and traces actuation.

⸻

1. Purpose (Normative)

ISPAD exists to answer one question only:

Is this external action permitted to occur now, and can it be audited without corrupting truth?

It prevents:
	•	silent execution,
	•	execution as implied authority,
	•	irreversible acts without explicit binding,
	•	action outcomes being mistaken for facts.

⸻

2. Scope (LOCKED)

ISPAD applies to any attempt to execute an UPAD EXECUTION_REQUEST.

ISPAD does NOT apply to:
	•	creating requests (UPAD),
	•	deciding (THIRD SPACE),
	•	finalizing truth (PoP),
	•	writing immutable history (SPIRAL),
	•	live presence custody (BNK),
	•	narration (22).

⸻

3. Execution Conditions (MANDATORY)

An execution is permitted only if ALL are true:
	1.	Request Validity
	•	UPAD request is well-formed
	•	action type ∈ closed set
	•	scope declared
	2.	Preconditions True
	•	machine-checkable guards evaluate true
	•	EVENT state constraints satisfied
	•	capacity constraints satisfied if relevant
	3.	PROPORTION Pass
	•	PROPORTION ≠ BLOCK/HALT at execution checkpoint
	4.	Authority Bound
	•	required role is present and authorized
	•	no identity is processed (role only)
	5.	Visibility
	•	execution produces an auditable record
	•	silent execution is forbidden

If any condition fails → execution MUST NOT occur.

⸻

4. IAM.MAI Coupling (Irreversibility)

If requested_action_type implies irreversible external change (examples: settlement triggers, permanent access revocation, event phase transitions), ISPAD MUST require:
	•	explicit human invocation, AND
	•	IAM.MAI FINALIZE reference (or an equivalent CANON-defined legitimacy gate)

ISPAD does not replace IAM.MAI.
ISPAD enforces its necessity when irreversibility is at stake.

⸻

5. Core Object: EXECUTION_RECORD (Closed Set)

A valid EXECUTION_RECORD MUST include:
	•	execution_id (opaque)
	•	request_id (UPAD)
	•	executor_system_id (system/service identifier; not a person)
	•	execution_ts
	•	execution_outcome ∈ {SUCCESS, FAIL, PARTIAL, REFUSED}
	•	outcome_refs (receipts, transaction hashes, logs — implementation-defined)
	•	authority_role_used (role label only)
	•	iam_mai_ref (required if irreversibility gated)
	•	lineage_ref (optional, for EVOLVE)

Forbidden fields
	•	identity
	•	inferred intent
	•	narrative justification
	•	statements that execution proves truth
	•	retroactive edits to prior records

⸻

6. Relationship to SPIRAL / Truth

ISPAD records are not truth.
	•	ISPAD MAY be referenced by THIRD SPACE decisions.
	•	ISPAD MUST NOT write truth directly.
	•	If an executed action must become immutable history, that must occur via separate legitimate SPIRAL append rules, with IAM.MAI gating where required.

Action trace ≠ truth.

⸻

7. Relationship to Other Protocols
	•	UPAD: provides request object.
	•	PROPORTION: gates authorization.
	•	IAM.MAI: required for irreversible classes.
	•	EVENT: constrains temporal admissibility.
	•	SPIRAL: may append only if independently legitimized; ISPAD itself does not “make history.”
	•	22: MAY narrate aggregate execution stats only (never per-request).

⸻

8. Failure Modes (EXPLICIT)

NON-COMPLIANT:
	•	executing when PROPORTION = BLOCK/HALT,
	•	executing without producing an EXECUTION_RECORD,
	•	using identity to satisfy authority,
	•	allowing automated execution where human invocation is mandated,
	•	letting execution outcomes rewrite facts or history,
	•	persisting targeted logs that imply identity.

⸻

9. Canonical One-Line Definition

ISPAD is the protocol that authorizes and audits external execution from UPAD requests under proportion and legitimacy constraints, without creating truth or identity.

⸻

END — ISPAD.md
