# Structural Explainability (SE)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/license/MIT)
![Build Status](https://github.com/structural-explainability/spec-se/actions/workflows/ci-md.yml/badge.svg?branch=main)
[![Check Links](https://github.com/structural-explainability/spec-se/actions/workflows/links.yml/badge.svg)](https://github.com/structural-explainability/spec-se/actions/workflows/links.yml)
[![Dependabot](https://img.shields.io/badge/Dependabot-enabled-brightgreen.svg)](https://github.com/structural-explainability/spec-se/security)

> Authoritative specification of Structural Explainability (SE).

## Overview

The Structural Explainability (SE) specification defines the minimal,
interpretation-neutral constraints under which identity, structure, change,
explanation, and disagreement can coexist over time.

SE establishes a shared representational substrate that remains stable across
incompatible epistemic, causal, and normative frameworks.

## Purpose

The purpose of SE is to define
**the conditions under which explanation is possible without being embedded**.

SE enables external frameworks to
explain, evaluate, or judge recorded structures
while preventing those interpretations from being asserted as substrate facts.

SE concerns representation only.
It does not determine meaning, correctness, or responsibility.

## Scope

This specification defines:

- neutrality constraints on representation
- explicit identity and persistence requirements
- structured, non-destructive representation of change
- boundaries between structure and interpretation

This specification does NOT define:

- causal explanations or mechanisms
- epistemic truth or validation
- normative judgment or enforcement
- domain vocabularies or application semantics
- decision-making or optimization logic

## Position in the Stack

SE is the foundational substrate.

- Structural Explainability (SE) defines admissible representation constraints.
- Accountable Entities (AE) refine identity and persistence regimes.
- Evolution Protocol (EP) defines structural change over time.
- Contextual Evidence & Explanations (CEE) attach interpretation above the substrate.

No downstream specification may weaken or override SE constraints.

## Relationship to Other Specifications

- SE is **foundational** and has no upstream dependencies.
- AE, EP, and CEE are defined as downstream specifications.
- All downstream specifications MUST conform to SE neutrality constraints.
- Interpretation, explanation, and evaluation occur strictly outside SE.

## Repository Contents

- [SPEC.md](./SPEC.md) - Normative specification
- [SPEC_LAYERS.md](./SPEC_LAYERS.md) - Canonical epistemic layer model and definitions
- [IDENTIFIERS.md](./IDENTIFIERS.md) - Stable requirement identifiers
- [CONFORMANCE.md](./CONFORMANCE.md) - Conformance checklist
- [se-manifest-1.md](./manifests/se-manifest-1.md) - SE manifest schema and field definitions
- [ANNOTATIONS.md](./ANNOTATIONS.md) - Annotation standards
- [LICENSE](./LICENSE) - licensing terms
- [CITATION.cff](./CITATION.cff) - Citation metadata
- [CHANGELOG.md](./CHANGELOG.md) - Version history

## Clarifying Statement

Structural Explainability defines what may be represented and
how it may change, without asserting
what is known, why it happened, or what ought to be done.

By separating structure from interpretation, SE ensures that:

- shared structural history remains stable and neutral,
- incompatible explanations may coexist without contradiction,
- accountability is preserved under persistent disagreement.

SE enables explanation without becoming explanatory.

## Developer (running pre-commit)

Steps to run pre-commit locally. Install `uv`.

Initialize once:

```shell
uv self update
uvx pre-commit install
uvx pre-commit run --all-files
```

Save progress as needed:

```shell
git add -A
# If pre-commit makes changes, re-run `git add -A` before committing.
git commit -m "update"
git push -u origin main
```
