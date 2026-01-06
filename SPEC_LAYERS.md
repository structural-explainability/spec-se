# Structural Explainability Layer Model (SPEC_LAYERS)

- Status: Normative
- Applies to: Structural Explainability specifications, formalizations, and implementations
- Audience: Humans (reviewers, maintainers, instructors); machines by reference
- Purpose: Define the canonical epistemic layer taxonomy used by SE-governed repositories

## 1. Purpose

This document defines the **Structural Explainability (SE) layer model**.

Layers classify repositories by their **epistemic position**:
what kind of claims they are permitted to make and what kinds they must not.

The layer model is used by:

- SE specifications
- SE formalizations
- SE implementations
- Repositories declaring SE alignment via `SE_MANIFEST.toml`

This document defines **layer meanings**.
Manifests simply **declare** layer membership.

## 2. Normative Scope

This document is **normative** for repositories governed by Structural Explainability.

It defines:

- the canonical set of `layer.space` values for SE
- the intended meaning of each layer
- permitted and prohibited activities at each layer

It does **not**:

- define repository metadata schemas
- enforce validation rules
- define domain-specific layer vocabularies (e.g., education, analytics)

## 3. Canonical SE Layer Spaces

The following table defines the **closed set** of SE canonical layer spaces.

| `layer.space`  | Definition                           | Permitted                                       | Prohibited                     |
| -------------- | ------------------------------------ | ----------------------------------------------- | ------------------------------ |
| Foundation     | Fundamental invariants and axioms    | Structural definitions; identity rules          | Interpretation; domain meaning |
| Protocol       | Neutral exchange structures          | Record formats; envelopes; dependency structure | Explanation; evaluation        |
| Specification  | Normative structural constraints     | “Must / must not” rules; invariants             | Execution; interpretation      |
| Formalization  | Machine-checked representations      | Proofs; type encodings                          | New semantics; interpretation  |
| Implementation | Executable realizations of specs     | Code; validators; builders                      | Silent interpretation          |
| Application    | Purpose-bound use of implementations | Optimization; interpretation; narrative         | Claims of general validity     |
| Governance     | Institutional or procedural control  | Policies; review rules; constraints             | Redefinition of structures     |

This table is **normative**.

Repositories governed by SE **must not invent additional SE layer spaces**.

## 4. Canonical Layer Roles

Layer roles describe the **function** of a repository _within_ a layer.
Roles are **descriptive**, not hierarchical.

Common SE roles include:

| `layer.role`   | Description                          |
| -------------- | ------------------------------------ |
| foundation     | Defines or anchors invariants        |
| reference      | Authoritative definition or exemplar |
| boundary       | Defines admissible scope or limits   |
| adapter        | Translates or maps between forms     |
| validator      | Checks conformance                   |
| curriculum     | Instructional use                    |
| demonstration  | Illustrative or exploratory use      |
| infrastructure | Supporting tooling                   |

This list is **open but governed**.

New roles may be introduced if they:

- do not redefine layer semantics
- do not contradict the layer's permitted activities

## 5. External Layer Vocabularies

Structural Explainability **does not own all layer vocabularies**.

Repositories may declare `layer.space` and `layer.role` values defined by
**external vocabularies**, such as:

- Data Analytics
- Education
- Domain-specific research programs

When doing so:

- The governing vocabulary **must be clear from context**
- SE semantics do **not** apply beyond the manifest declaration
- Such declarations do **not** expand SE's canonical layer set

Example (external vocabulary):

```toml
[layer]
space = "Data Analytics"
role  = "post-secondary-education"
```

This is valid in `SE_MANIFEST.toml` but **not governed by this document**.

## 6. Relationship to SE_MANIFEST

`SE_MANIFEST.toml` uses this document by reference.

- The manifest declares `layer.space` and `layer.role`
- This document defines what those values mean **when governed by SE**
- Manifests do not redefine layer semantics

This separation is intentional and normative.

## 7. Change Control

This layer model is versioned as part of the
Structural Explainability Specification.

Changes to canonical SE layers require:

- explicit revision of this document
- review for downstream impact

Manifests reference layer values but do not control their definition.
