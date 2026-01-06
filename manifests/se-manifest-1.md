# SE Manifest Specification (se-manifest-1)

- Status: Normative
- Layer: Specification
- Applies to: Repositories declaring Structural Explainability alignment
- Schema Identifier: `se-manifest-1`

## 1. Purpose and Role

An **SE Manifest** is a declarative, repository-level claim card.

Its purpose is to make explicit:

- what a repository claims to be,
- where it sits in the epistemic stack,
- what it depends on,
- what it intentionally provides,
- what is explicitly in scope and out of scope,
- how it should be cited,
- and how it traces to external specifications or identifiers.

The manifest is **human-legible**, **machine-readable**, and **reviewable**.
It enables accountability, composability, and disagreement without requiring
interpretation of repository contents.

The manifest does **not** assert correctness, truth, or endorsement.

## 2. Boundaries and Non-Goals

The SE Manifest **does not**:

- define Structural Explainability principles or constraints,
- replace `README.md` documentation,
- encode build, execution, or deployment configuration,
- contain interpretive claims, observations, or conclusions,
- replace citation metadata (`CITATION.cff`),
- replace disclosure, provenance, or attestation appendices.

### Relationship to Other Artifacts

| Artifact           | Role                                                  |
| ------------------ | ----------------------------------------------------- |
| `SE_MANIFEST.toml` | Declares repository intent, scope, and position       |
| `CITATION.cff`     | Defines citation metadata and attribution             |
| SE Appendix        | Records observations, interpretive claims, provenance |
| SE Specifications  | Define normative principles, constraints, identifiers |

The manifest may **reference** these artifacts but does not subsume them.

## 3. File Format and Identification

The manifest is typically stored as `SE_MANIFEST.toml`.

Each manifest **must** declare the schema identifier:

```toml
schema = "se-manifest-1"
```

This identifier denotes conformance to this specification document.

## 4. Attribute Definitions

### 4.1 `[repo]` - Repository Identity

Declares the stable identity and intent of the repository.

| Field   | Required | Type   | Description                                                           |
| ------- | -------- | ------ | --------------------------------------------------------------------- |
| name    | Yes      | string | Repository name                                                       |
| org     | Yes      | string | Owning organization or account                                        |
| kind    | Yes      | string | High-level repository kind (e.g. `software`, `spec`, `formalization`) |
| status  | Yes      | string | Lifecycle status (e.g. `academic`, `normative`, `reference`)          |
| since   | Yes      | string | Initial year of the repository                                        |
| summary | Yes      | string | One-sentence description of purpose                                   |

### 4.2 `[layer]` - Epistemic Position

Declares where the repository sits in the Structural Explainability stack.

| Field | Required | Type   | Description                       |
| ----- | -------- | ------ | --------------------------------- |
| space | Yes      | string | Epistemic layer                   |
| role  | Yes      | string | Functional role within that layer |

Allowed values for `layer.space` and `layer.role` are **defined normatively**
in the Structural Explainability specification (see `SPEC_LAYERS.md`).

Manifests **declare** a layer; they do not define layer semantics.

### 4.3 `[depends]` - Declared Dependencies

Declares upstream commitments.

| Field    | Required | Type         | Description                                              |
| -------- | -------- | ------------ | -------------------------------------------------------- |
| required | Yes      | list[string] | Dependencies required to interpret or use the repository |
| optional | Yes      | list[string] | Optional tools or integrations                           |

An empty list indicates no declared dependencies.

### 4.4 `[provides]` - Intended Artifacts

Declares which artifacts are intentionally provided and maintained.

| Field     | Required | Type         | Description                                                       |
| --------- | -------- | ------------ | ----------------------------------------------------------------- |
| artifacts | Yes      | list[string] | Files or directories considered part of the repository’s contract |

This section supports review, automation, and governance checks.

### 4.5 `[scope]` - Semantic Boundary

Defines what the repository explicitly includes and excludes.

| Field    | Required | Type         | Description                                          |
| -------- | -------- | ------------ | ---------------------------------------------------- |
| includes | Yes      | list[string] | In-scope concepts, behaviors, or responsibilities    |
| excludes | Yes      | list[string] | Explicitly out-of-scope concepts or responsibilities |

Scope declarations are normative and intended to prevent scope creep,
misinterpretation, and inappropriate reuse.

### 4.6 `[citation]` - Citation Pointer

Declares how the repository should be cited.

| Field     | Required | Type   | Description                                              |
| --------- | -------- | ------ | -------------------------------------------------------- |
| cff       | Yes      | string | Path to `CITATION.cff`                                   |
| preferred | Yes      | string | Preferred citation target (e.g. `repo`, `spec`, `paper`) |
| bib_hint  | No       | string | Optional bibliographic identifier hint                   |

### 4.7 `[traceability]` - Identifier Resolution

Declares how identifiers referenced by the repository are resolved.

| Field          | Required | Type   | Description                                             |
| -------------- | -------- | ------ | ------------------------------------------------------- |
| identifier_map | Yes      | string | Path or value describing identifier resolution strategy |

A value of `"none"` indicates no external identifier resolution is declared.

## 5. Normative Status

This document defines the **normative meaning** of `se-manifest-1`.

Manifests claiming this schema **must** conform to the attribute definitions
and boundaries described here.

Examples are illustrative and non-normative.

## 6. Change Control

Revisions to this specification are versioned in the
Structural Explainability Specification repository.

Manifests should reference the schema identifier, not a mutable interpretation.
