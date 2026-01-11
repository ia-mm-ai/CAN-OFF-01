UPAD - Unified Action Dispatch Protocol

SProtocol-ID: P.14.UPAD  
Filename: 14__UPAD.md  
Status: CANONICAL  
Class: Decision → Execution Request Boundary  
Mutation: EVOLVE ONLY

---

0. Canonical Statement

UPAD governs how a decision becomes a request for external action without becoming authority or execution.

UPAD creates an EXECUTION_REQUEST object that can be accepted or refused by an external executor, while preventing:
	•	decisions from smuggling instructions,
	•	language from implying mandate,
	•	identity from entering actuation.

UPAD does not execute.
UPAD requests.

⸻

1. Purpose (Normative)

UPAD exists to answer one question only:

What is being requested to happen, under what declared scope, with what prerequisites?

It prevents:
	•	implicit execution,
	•	“decision-as-command” leakage,
	•	retroactive rationalization,
	•	scope expansion through phrasing.

⸻

2. Scope (LOCKED)

UPAD applies only after:
	•	BPL admits the input,
	•	a DECISION_RECORD exists in THIRD SPACE (or an explicit authorized request exists),
	•	PROPORTION = OK/WARN at request-creation checkpoint.

UPAD does NOT apply to:
	•	executing the action (ISPAD handles legitimacy + audit),
	•	finalizing truth (PoP, SPIRAL),
	•	live presence custody (BNK),
	•	narration (22).

⸻

3. Core Object: EXECUTION_REQUEST (Closed Set)

A valid EXECUTION_REQUEST MUST include:
	•	request_id (opaque)
	•	decision_id (THIRD SPACE) OR request_source = EXTERNAL_AUTHORIZED
	•	referenced_fact_ids (SPIRAL ids only; may be empty)
	•	requested_action_type (enum, closed set below)
	•	requested_action_scope (time/container/system boundary)
	•	preconditions (machine-checkable guards; may include PROPORTION state, EVENT state)
	•	required_authority_role (role label; no identity)
	•	created_ts
	•	lineage_ref (optional, for EVOLVE)

Forbidden fields
	•	identity (names, addresses, wallets, device IDs)
	•	directives framed as necessity (“must”, “required to do X now”)
	•	inferred intent
	•	narrative justification
	•	execution endpoints (implementation-specific routing must be external)

⸻

4. Action Types (Closed Set)

requested_action_type MUST be exactly one of:
	•	ADMIT
	•	DENY
	•	GRANT_ACCESS
	•	REVOKE_ACCESS
	•	ISSUE_ARTIFACT
	•	REVOKE_ARTIFACT
	•	TRIGGER_SETTLEMENT
	•	TRIGGER_REFUND
	•	NOTIFY_AGGREGATE
	•	START_PROCESS
	•	STOP_PROCESS

No other types are valid without CANON update.

⸻

5. Preconditions (Allowed)

Preconditions MAY reference:
	•	EVENT state (0 / ⊙ / 1)
	•	ZIVai state (LOW/MED/HIGH/SATURATED)
	•	PROPORTION state (OK/WARN only for issuance; BLOCK/HALT forbids)
	•	IAM.MAI requirement flag (if action implies irreversibility)
	•	required external receipts (implementation-defined)

Preconditions MUST NOT reference identity.

⸻

6. UPAD Output Semantics

UPAD outputs EXECUTION_REQUEST only if:
	•	BPL compliant,
	•	THIRD SPACE reference valid (or external authorized source),
	•	PROPORTION not BLOCK/HALT,
	•	scope declared and non-expanding,
	•	action type is in closed set.

Otherwise UPAD MUST output: REFUSE_CREATE_REQUEST.

⸻

7. Relationship to Other Protocols
	•	THIRD SPACE: provides decision_id and lineage.
	•	SPIRAL: may provide referenced_fact_ids.
	•	PROPORTION: gates request creation.
	•	ISPAD: consumes UPAD requests for authorization/execution trace.
	•	IAM.MAI: may be required downstream for irreversible actions; UPAD does not invoke it.

⸻

8. Failure Modes (EXPLICIT)

NON-COMPLIANT:
	•	generating execution requests from narration,
	•	including identity or target-specific identifiers,
	•	creating a request when PROPORTION = BLOCK/HALT,
	•	using free-text action types,
	•	encoding execution endpoints inside the request,
	•	allowing “implicit mandate” language.

⸻

9. Canonical One-Line Definition

UPAD is the protocol that converts decisions into non-binding execution requests with declared scope, without authority, identity, or execution.

⸻

END — UPAD.md
