# Structural Explainability Identifiers (SE)

This document defines the stable requirement identifiers used by the
Structural Explainability (SE) specification.

Identifiers are the sole normative reference mechanism.
Section ordering, formatting, and presentation are non-normative.

## Overview

Defines the foundational neutrality constraints
for shared representational substrates,
under which downstream specifications operate without
embedding epistemic, causal, or normative interpretation.

## Identifier Semantics and Ordering

Identifiers are the sole normative reference mechanism.
Section ordering, formatting, and presentation are non-normative.

Identifiers are listed in strict alphabetical order to remove
editorial discretion and ensure deterministic placement.

## Identifier Naming Rules

All identifiers follow this pattern:

SE.<CATEGORY>.<SUBCATEGORY>.<QUALIFIER>

Identifiers are:

- semantic, not positional
- stable across versions
- reusable across prose, code, and formal proofs
- language-agnostic
- suitable for direct mapping to Lean theorem names

Identifiers MUST NOT be renamed or repurposed.
New identifiers MAY be added only in a new major version of this document.

## Identifier Notes

Each identifier MUST be followed by exactly one note.

- The note MUST be expressed as a single bullet.
- The bullet text MAY wrap across lines.
- No additional bullets, sublists, or structural markers are permitted.
- Notes are explanatory only and do not introduce additional requirements.

## Canonical Identifier List (Alphabetical, with Notes)

SE.BOUNDARY.NON_OWNERSHIP

- Requires that the substrate does not resolve, privilege, or own epistemic,
causal, or normative interpretations.

SE.BOUNDARY.RESPONSIBILITY

- Requires that epistemic, causal, and normative responsibility reside outside
the substrate.

SE.CANONICAL.RULE

- Defines the separation of structural recording from external interpretation,
evaluation, and judgment.

SE.CHANGE.DEPENDENCY

- Permits representation of structural dependency without causal explanation.

SE.CHANGE.NON_MUTATION

- Prohibits implicit mutation of prior state and requires structural traceability.

SE.CHANGE.STRUCTURED

- Requires change to be represented explicitly as a structured phenomenon.

SE.DEFINITION.CORE

- Defines Structural Explainability as a neutral representational property
enabling explanation by external frameworks.

SE.IDENTITY.DISTINCT

- Requires entity identity to be distinct from state, version, or interpretation.

SE.IDENTITY.EXPLICIT

- Requires identity conditions to be explicitly represented.

SE.IDENTITY.PERSISTENCE

- Requires identity persistence rules to be explicit and structurally checkable.

SE.NEUTRALITY.CAUSAL.ALLOWED

- Enumerates causal-related representations permitted without explanation.

SE.NEUTRALITY.CAUSAL.PROHIBITED

- Prohibits assertion of causal mechanisms or production relations.

SE.NEUTRALITY.EPISTEMIC.ALLOWED

- Enumerates epistemic-related representations permitted without judgment.

SE.NEUTRALITY.EPISTEMIC.PROHIBITED

- Prohibits assertion of truth, validity, or evidentiary sufficiency.

SE.NEUTRALITY.NORMATIVE.ALLOWED

- Enumerates normative-related representations permitted without authority.

SE.NEUTRALITY.NORMATIVE.PROHIBITED

- Prohibits encoding of obligations, permissions, enforcement, or evaluation.

SE.NON_GOALS.EXCLUDED

- Defines what Structural Explainability explicitly does not do.

SE.TIME.EXPLICIT

- Requires temporal persistence to be explicitly represented.

SE.TIME.NON_DESTRUCTIVE

- Prohibits destructive overwrite of historical state.

SE.TIME.NON_GLOBAL

- Prohibits assumption of a global time semantics.

## Cross-Artifact Consistency Rule

Each identifier in this list MUST appear:

- exactly once in SPEC.md
- exactly once in CONFORMANCE.md
- exactly once as a field in the Lean `ConformanceEvidence` structure
- exactly once in the Lean requirements list

Alphabetical order SHOULD be preserved across all artifacts.
