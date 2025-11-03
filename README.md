# Markdown Software Design Description (MSDD)

A modern, structured markdown template for **Software Design Description (SDD)** documents aligned with **IEEE 1016™-2009** and **ISO/IEC/IEEE 42010:2011**.
It complements the [Markdown Software Requirements Specification (MSRS)](https://github.com/jam01/SRS-Template) by shifting focus from *what the system must do* to *how the system will be built*.

This template helps teams articulate the **architecture, design rationale, and key decisions** of a system in a format that is:

* Developer-friendly and reviewable in Git
* Traceable to requirements and decisions
* AI-interpretable and automation-ready

## Highlights

* **Standards-aligned:** IEEE 1016™-2009 (SDD) and ISO/IEC/IEEE 42010 (Architecture Description)
* **Comprehensive, viewpoint-based design structure**
* **Built-in prompts and guidance** to improve clarity and consistency
* **Traceability-ready:** Cross-reference requirements (SRS) and decisions (MADR)
* **Suitable for modern architectures:** cloud, microservices, ML/AI, DevOps
* **Readable, version-controlled, and exportable** (e.g., Markdown → PDF/HTML)

## Who Should Use This

* **Software architects and engineers** defining system structure and interactions
* **Developers** implementing or maintaining the design
* **Operators and SREs** understanding deployment, topology, and runtime behavior
* **QA, compliance, and audit teams** verifying design conformance to requirements

## Quick Start

1. Copy `sdd-template.mdd` into your repository (e.g., `docs/sdd.md`).
2. Fill in the document metadata (project name, version, author, organization, date).
3. Complete Section 1 to establish context, scope, glossary, and references.
4. Use Section 2 to outline design strategy, stakeholders, and selected viewpoints.
5. Document concrete architectural and design **views** in Section 3.
6. Record significant **decisions** and their rationale in Section 4 (MADR-compatible).
7. Add any supporting materials or models in **Appendixes**.
8. Keep the **revision history** in sync with your VCS releases.

## Template Structure (Overview)

1. **Introduction:** Purpose, scope, glossary, references, and document conventions
2. **Design Overview:** Stakeholders, concerns, and chosen viewpoints
3. **Design Views:** Prescriptive or descriptive architecture, decomposed by viewpoint
4. **Decisions:** Key architectural and design decisions with context and rationale
5. **Appendixes:** Supporting, non-normative materials (models, data, examples)

Each section contains clear guidance, examples, and tips for effective use.

## Recommended Workflows

### One-Shot Project Document

* Fill out `sdd-template.mdd` as a single document.
* Export to PDF/HTML via pandoc and distribute to stakeholders.

### Living Design Document (Version-Controlled)

* Keep `sdd-template.mdd` as `docs/sdd.md` in your repo.
* Incrementally update design sections as architecture evolves.
* Sync SDD and SRS versions; reference requirement IDs from the SRS.
* Cross-link design decisions (Section 4) to Architecture Decision Records (ADRs).

### Modular Architecture Documentation

* Maintain an SDD plus individual design view files under `docs/design/`.
* Use `docs/decisions/` for MADR-style decision records.
* Reference design views and decisions from Section 3 and Section 4 indexes.

## Integration with SRS and ADRs

| Artifact        | Purpose                                          | Format                                  |
| --------------- | ------------------------------------------------ |-----------------------------------------|
| **SRS (MSRS)**  | Defines *what* the system must do                | `docs/srs.md`, `docs/requirements/*.md` |
| **SDD (MSDD)**  | Defines *how* the system is built                | `docs/sdd.md`, `docs/design/*.md`       |
| **ADRs (MADR)** | Records *why* certain design decisions were made | `docs/decisions/*.md`                   |

This triad supports full traceability: **requirements → design → decisions**.

## Related Projects

* [Markdown Software Requirements Specification (MSRS)](https://github.com/jam01/SRS-Template)
* [Markdown Architecture Decision Records (MADR)](https://adr.github.io/madr/)

## License

This template is dedicated to the public domain under the
[Creative Commons Zero v1.0 Universal (CC0 1.0)](https://creativecommons.org/publicdomain/zero/1.0/) license.

You may copy, modify, distribute, and use it freely—even for commercial purposes—without permission.
