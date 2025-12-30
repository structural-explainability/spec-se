# Structural Explainability Specification (SE)

Status: Normative

This document defines the normative constraints for conformance with
Structural Explainability (SE).

## How to Read This Spec

Keywords MUST, MUST NOT, SHOULD, and MAY
are to be interpreted as described in RFC 2119.

Use of terms such as "canonical" denotes structural role only and
does not imply epistemic, causal, or normative preference.

This specification does not prescribe editorial structure,
terminology preference, or documentation layout beyond identifier semantics.

## Representation vs Constraint Classes

Some requirements describe what the substrate MAY represent,
while others constrain how such representations MUST NOT be interpreted.

Overlap between these classes is intentional:
representation permissions do not imply explanatory commitment.

## Identifier Semantics and Stability

Each requirement in this document is identified by a stable identifier
of the form `SE.*`.

Identifiers are the sole normative reference for conformance.
Textual wording MAY be clarified over time without changing meaning;
any change that alters the requirement MUST result in a new identifier.

Renaming, reordering, or relocating identifiers constitutes a semantic
change and is therefore intentionally diff-visible.

Repository paths, filenames, and section ordering are non-normative and
do not affect identifier meaning.

---

## SE.BOUNDARY.NON_OWNERSHIP

The representational substrate MUST NOT resolve, privilege, or own
epistemic, causal, or normative interpretations.

Interpretations MAY be recorded as external references but remain external
to the substrate.

## SE.BOUNDARY.RESPONSIBILITY

Epistemic responsibility MUST reside outside the substrate.

Causal responsibility MUST reside outside the substrate.

Normative responsibility MUST reside outside the substrate.

## SE.CANONICAL.RULE

It records what exists and how it changes.
External frameworks determine what is known, why it happened,
and what ought to be done.

Canonical here denotes structural scope and separation of concerns,
not preference, authority, or correctness.

## SE.CHANGE.DEPENDENCY

The substrate MAY represent structural dependency relationships.

Such dependencies MUST NOT be asserted as causal explanations.

## SE.CHANGE.NON_MUTATION

Change MUST NOT be encoded as implicit mutation of prior state.

Prior states MUST remain structurally accessible or reconstructible.

## SE.CHANGE.STRUCTURED

Change MUST be represented as a structured phenomenon
(e.g., event, exchange).

Change representation MUST be explicit and non-destructive.

## SE.DEFINITION.CORE

Structural Explainability is the property of a representational system
whose structure enables entities and their change over time to be
explained by external frameworks, while remaining neutral with respect
to epistemic truth, causal explanation, and normative judgment.

## SE.IDENTITY.DISTINCT

Entity identity MUST be distinguishable from state, version,
interpretation, or descriptive attributes.

## SE.IDENTITY.EXPLICIT

Entities MUST be represented with explicit identity conditions.

Identity MUST NOT be implicit or inferred.

## SE.IDENTITY.PERSISTENCE

Rules governing identity persistence over time MUST be explicitly
declared and structurally checkable.

## SE.NEUTRALITY.CAUSAL.ALLOWED

The substrate MAY represent temporal order.

The substrate MAY represent structural dependency without explanation.

The substrate MAY record references to external causal explanations.

## SE.NEUTRALITY.CAUSAL.PROHIBITED

The substrate MUST NOT assert that one entity, event, or state
produced another.

The substrate MUST NOT encode causal mechanisms or explanations.

The substrate MUST NOT rely on counterfactual dependence.

## SE.NEUTRALITY.EPISTEMIC.ALLOWED

The substrate MAY record that claims exist.

The substrate MAY record attribution, scope, and provenance.

Epistemic judgment MUST be deferred to external frameworks.

## SE.NEUTRALITY.EPISTEMIC.PROHIBITED

The substrate MUST NOT assert truth, correctness, or validity of claims.

The substrate MUST NOT assert evidentiary sufficiency, confidence,
or reliability.

The substrate MUST NOT encode verification or validation as substrate facts.

## SE.NEUTRALITY.NORMATIVE.ALLOWED

The substrate MAY represent rules, policies, or norms as entities.

The substrate MAY record scope or applicability without judgment.

Normative authority MUST be deferred to external institutions.

## SE.NEUTRALITY.NORMATIVE.PROHIBITED

The substrate MUST NOT encode obligations, permissions, or prohibitions.

The substrate MUST NOT assert compliance, violation, or enforcement.

The substrate MUST NOT prescribe actions or evaluations.

## SE.NON_GOALS.EXCLUDED

It does not explain outcomes.

It does not determine correctness.

It does not resolve disagreement.

It does not automate decision-making.

It does not enforce rules or policies.

## SE.TIME.EXPLICIT

Temporal persistence MUST be explicitly represented.

Time MUST NOT be implicit.

## SE.TIME.NON_DESTRUCTIVE

Prior states MUST NOT be overwritten without structural trace.

Historical states MUST remain accessible or reconstructible.

## SE.TIME.NON_GLOBAL

Time MUST NOT be assumed to be global.

Temporal interpretation MUST remain external.
