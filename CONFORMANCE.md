# Conformance Checklist

This document defines the criteria for determining whether an artifact
conforms to the Structural Explainability specification.

Identifiers referenced in this document are the sole normative reference.
Ordering and formatting are non-normative.

An artifact may be a specification, schema, implementation, repository,
or other deliverable claiming conformance.

## Conformance Overview

An artifact CONFORMS if and only if:

- all mandatory requirements are satisfied
- no prohibited assertions are present
- no downstream interpretation is embedded in the substrate

Failure of any single check constitutes non-conformance.

SE.BOUNDARY.NON_OWNERSHIP

- [ ] The artifact does not resolve, privilege, or own epistemic interpretations.
- [ ] The artifact does not resolve, privilege, or own causal interpretations.
- [ ] The artifact does not resolve, privilege, or own normative interpretations.
- Fail if: interpretive conclusions are embedded as substrate facts.

SE.BOUNDARY.RESPONSIBILITY

- [ ] Epistemic responsibility is not assigned by the substrate.
- [ ] Causal responsibility is not assigned by the substrate.
- [ ] Normative responsibility is not assigned by the substrate.
- Fail if: responsibility is attributed within the substrate layer.

SE.CANONICAL.RULE

- [ ] The artifact records structural existence and change only.
- [ ] Determinations of knowledge, cause, or obligation are externalized.
- Fail if: the artifact prescribes interpretation, explanation, or evaluation.

SE.CHANGE.DEPENDENCY

- [ ] Structural dependency relationships may be represented.
- [ ] Dependencies are not asserted as causal explanations.
- Fail if: dependency is used to imply causation or justification.

SE.CHANGE.NON_MUTATION

- [ ] Change is not encoded as implicit mutation of prior state.
- [ ] Prior states remain structurally accessible or reconstructible.
- Fail if: state is overwritten without structural trace.

SE.CHANGE.STRUCTURED

- [ ] Change is represented as an explicit structured phenomenon.
- [ ] Change representation is non-destructive.
- Fail if: change is implicit, inferred, or destructive.

SE.DEFINITION.CORE

- [ ] The artifact treats Structural Explainability as a neutrality constraint.
- [ ] The artifact enables explanation only by external frameworks.
- Fail if: the artifact embeds epistemic truth, causal explanation,
  or normative judgment.

SE.IDENTITY.DISTINCT

- [ ] Entity identity is distinguishable from state or description.
- [ ] Identity is not conflated with interpretation or versioning.
- Fail if: identity is inferred or derived implicitly.

SE.IDENTITY.EXPLICIT

- [ ] Identity conditions are explicitly represented.
- [ ] Identity is not inferred from context or attributes.
- Fail if: identity is implicit or heuristic.

SE.IDENTITY.PERSISTENCE

- [ ] Identity persistence rules are explicitly declared.
- [ ] Persistence rules are structurally checkable.
- Fail if: persistence depends on interpretation or convention.

SE.NEUTRALITY.CAUSAL.ALLOWED

- [ ] Temporal order may be represented.
- [ ] Structural dependency may be represented without explanation.
- [ ] References to external causal explanations may be recorded.
- Fail if: causal mechanisms or production relations are asserted.

SE.NEUTRALITY.CAUSAL.PROHIBITED

- [ ] No entity, event, or state is asserted to produce another.
- [ ] No causal mechanisms are encoded.
- [ ] No counterfactual dependence is relied upon.
- Fail if: causation is represented as a substrate fact.

SE.NEUTRALITY.EPISTEMIC.ALLOWED

- [ ] Claims may be recorded as existing.
- [ ] Attribution, scope, and provenance may be recorded.
- Fail if: epistemic judgment is performed by the substrate.

SE.NEUTRALITY.EPISTEMIC.PROHIBITED

- [ ] Truth, correctness, or validity is not asserted.
- [ ] Evidentiary sufficiency or confidence is not asserted.
- [ ] Verification or validation is not encoded as substrate fact.
- Fail if: epistemic evaluation is embedded.

SE.NEUTRALITY.NORMATIVE.ALLOWED

- [ ] Rules, policies, or norms may be represented as entities.
- [ ] Scope or applicability may be recorded without judgment.
- Fail if: normative authority is asserted by the substrate.

SE.NEUTRALITY.NORMATIVE.PROHIBITED

- [ ] Obligations, permissions, or prohibitions are not encoded.
- [ ] Compliance, violation, or enforcement is not asserted.
- [ ] Actions or evaluations are not prescribed.
- Fail if: normative judgment is embedded.

SE.NON_GOALS.EXCLUDED

Verify that the artifact does not:

- [ ] explain outcomes
- [ ] determine correctness
- [ ] resolve disagreement
- [ ] automate decision-making
- [ ] enforce rules or policies

Presence of any of the above constitutes non-conformance.

SE.TIME.EXPLICIT

- [ ] Temporal persistence is explicitly represented.
- [ ] Time is not implicit.
- Fail if: temporal assumptions are unstated or inferred.

SE.TIME.NON_DESTRUCTIVE

- [ ] Prior states are not overwritten without trace.
- [ ] Historical states remain accessible or reconstructible.
- Fail if: history is destructively modified.

SE.TIME.NON_GLOBAL

- [ ] Time is not assumed to be global.
- [ ] Temporal interpretation remains external.
- Fail if: a global or absolute time semantics is imposed.

## Final Determination

An artifact CONFORMS if:

- all checks above pass, and
- no prohibited assertions are present.

Otherwise, the artifact is NON-CONFORMANT.

## Conformance Declaration

Artifacts claiming conformance SHOULD include a declaration of the form:

```
Conforms to: SE Specification vx.y
```
