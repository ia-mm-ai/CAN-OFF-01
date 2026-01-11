PROPORTION - Continuity Constraint Protocol

Status: CANONICAL
Class: System Envelope / Continuity Constraint
Authority: BOUND (via CANON)
Execution Power: LIMITED (block / halt only)
Identity Power: NONE
Truth Power: NONE
Mutation Rule: Additive-only (via EVOLVE + CANON)

⸻

0. Canonical Statement

PROPORTION governs whether the stack is allowed to proceed without violating continuity.

It defines a small closed set of ratios and bounds that must remain stable between:
	•	internal claims and external effects,
	•	decision volume and field capacity,
	•	irreversibility and authority,
	•	evidence and confidence.

If PROPORTION fails, the system MUST block transitions and may enter HALT.

PROPORTION does not decide outcomes.
PROPORTION constrains admissibility of motion.

⸻

1. Purpose (Normative)

PROPORTION exists to answer one question only:

Is this system still operating within its declared continuity bounds?

It prevents:
	•	drift disguised as progress,
	•	execution pressure collapsing governance,
	•	evidence deficits being converted into action,
	•	append-only history being used to launder mistakes,
	•	silent expansion of scope across cycles.

⸻

2. Scope (LOCKED)

PROPORTION applies to all protocol boundaries where motion occurs, including:
	•	BPL admit/deny
	•	EVENT transitions
	•	IAM.MAI FINALIZE gates
	•	KAPIA crossing record creation
	•	PoP FINALIZE
	•	SPIRAL APPEND
	•	THIRD SPACE decision recording
	•	UPAD execution request creation
	•	ISPAD execution authorization and recording
	•	22 narration emission (aggregate only)

PROPORTION is system-wide.
It is not optional.

⸻

3. Proportion Variables (Closed Set)

PROPORTION MUST track exactly these envelope variables (no others):
	1.	CLAIM↔EVIDENCE
	•	claims must not exceed admissible evidence support
	2.	DECISION↔CAPACITY
	•	decision frequency must not exceed field capacity (via ZIVai state)
	3.	SCOPE↔DECLARATION
	•	no action or record may exceed declared scope
	4.	IRREVERSIBILITY↔AUTHORITY
	•	irreversible transitions require explicit authority (IAM.MAI where applicable)
	5.	MEMORY↔LEGITIMACY
	•	only legitimate finalized content becomes immutable (SPIRAL rules)

These variables are non-identitarian and aggregate by design.

⸻

4. Checkpoints (Mandatory)

PROPORTION MUST be evaluated at these checkpoints:

4.1 Admission checkpoints
	•	before BPL allows reasoning
	•	before THIRD SPACE records a decision
	•	before UPAD creates an execution request

4.2 Live checkpoints
	•	during EVENT ⊙, on pacing signals (ZIVai)
	•	before KAPIA writes a crossing record

4.3 Irreversible checkpoints
	•	before IAM.MAI FINALIZE is invoked
	•	before PoP FINALIZE
	•	before SPIRAL APPEND
	•	before ISPAD authorizes execution

⸻

5. Output (Closed Set)

At any checkpoint, PROPORTION MUST emit exactly one state:
	•	OK
	•	WARN
	•	BLOCK
	•	HALT

Semantics:
	•	OK: proceed
	•	WARN: proceed but require explicit visibility (22 MAY narrate aggregate)
	•	BLOCK: transition forbidden until revised
	•	HALT: stop processing; no downstream protocols may proceed

PROPORTION MUST NOT emit numeric scores.

⸻

6. Effects (Binding)
	•	If PROPORTION = OK/WARN → transition MAY proceed (if other guards pass)
	•	If PROPORTION = BLOCK → transition MUST NOT proceed
	•	If PROPORTION = HALT → reasoning, execution requests, finalization, narration MUST stop

PROPORTION may block.
PROPORTION may halt.
PROPORTION may not execute.

⸻

7. Authority & Power

PROPORTION:
	•	does NOT create truth,
	•	does NOT decide decisions,
	•	does NOT infer intent,
	•	does NOT encode identity,
	•	does NOT execute external actions.

PROPORTION only permits or refuses motion at boundaries.

⸻

8. Relationship to Other Protocols
	•	BPL: PROPORTION may tighten admissibility if semantic overload causes drift.
	•	EVENT: PROPORTION constrains pacing and irreversible transitions.
	•	ZIVai: PROPORTION consumes capacity state; never overrides ZIVai semantics.
	•	THIRD SPACE: PROPORTION blocks decisions that exceed evidence/scope.
	•	UPAD: PROPORTION blocks requests that exceed declared scope/authority.
	•	ISPAD: PROPORTION blocks execution that violates capacity/authority bounds.
	•	IAM.MAI: PROPORTION cannot replace IAM.MAI; it only conditions its invocation.
	•	SPIRAL: PROPORTION conditions append; SPIRAL enforces immutability.

⸻

9. Failure Modes (EXPLICIT)

NON-COMPLIANT:
	•	allowing motion when PROPORTION = BLOCK/HALT,
	•	adding new proportion variables outside closed set,
	•	emitting numeric scores,
	•	allowing identity-derived signals,
	•	treating WARN as authority,
	•	permitting irreversible transitions without authority binding.

⸻

10. Canonical One-Line Definition

PROPORTION is the system envelope that constrains all motion so continuity is preserved across time, without identity, authority leakage, or drift.

⸻

END — PROPORTION.md
