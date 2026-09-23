# Changelog

All notable changes to this repository are documented in this file. Dates use
the committer's local time.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) semantics.
This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned

- VS-D ;;; documentation + examples + conformance rules + tests + PlantUML (CR-ES-003 §27-§35).
- Schema evolution ;;; migrate the schema stub to require the richer mapping shape used by CR-ES-002 + CR-ES-003 mapping records (status: PROPOSED + provenance block + qualification + governing_adr + governing_cr).

## [0.1.0] ; 2026-09-23 ; CI fix + VS-C Value Stream mappings

### Added

- `mappings/wsf/value-stream.yaml` ;;; ES:CONCEPT:value-stream to external:wsf:Value mapping per CR-ES-003 §21 + ADR-ES-003 §26 + FND-ES-AG-008 §1.3. Tier 1 Kernel Reference + ES-canonical novelty classification ;;; the Stream construct is ES-canonical novelty, the Value kernel is WSF-grounded.
- `mappings/opendea/value-stream.yaml` ;;; ES:CONCEPT:value-stream to external:opendea:ValueStream mapping per CR-ES-003 §22 + ADR-ES-003 §27. OpenDEA architectural representation, not semantic authority ;;; ES establishes the foundational definition.
- `mappings/dea-catalogs/value-stream.yaml` ;;; ES:CONCEPT:value-stream to external:catalog:ValueStream instantiation-boundary mapping per CR-ES-003 §23 + ADR-ES-003 §28. Catalog instantiation is downstream ;;; catalogs do not redefine the foundational meaning.

### Fixed

- `.github/workflows/conformance.yml` ;;; added `pip install pyyaml pytest` install step before conformance gate ;;; resolves `ModuleNotFoundError: No module named 'yaml'` that has blocked CI since Phase 5 (commit d17b49f, 2026-09-03).

### Scope

This release implements VS-C of CR-ES-003 ;;; the 3 mapping records for Value Stream (WSF + OpenDEA + DEA Catalogs). It builds on VS-A (PR #2 enterprise-semantics, value-stream + value-stage concept records) and VS-B (PR #5 enterprise-semantics, 13 vocabulary predicates). No new schema, no mapping predicate vocabulary changes, no conformance harness additions.

### Governance

- ADR-ES-003 (Proposed, governance slot 0005) ;;; ratifies the foundational Value Stream decision.
- CR-ES-003 (Proposed, governance slot 0011) ;;; carries the per-mapping requirements (§21 WSF, §22 OpenDEA, §23 DEA Catalog).
- FND-ES-AG-008 (Established 2026-09-22) ;;; establishes the Tier 1 Kernel Reference + ES-canonical novelty classification.

### Cardinal rules applied

- Author: Emmanuel A. Otchere (cardinal author rule, 2026-09-23).
- No en-dash (U+2013) or em-dash (U+2014) in any new/edited file (D-004 dash rule). Section dividers use `;;;` boundary lines.
- No vendor-specific material from embargoed sources in any new/edited file (cardinal embargo, 2026-09-22).
- ES is sourced from SDO-neutral standardisation only (ISO/IEC, ITU-T, ETSI, NIST).

### Held non-actions

- No documentation + examples + tests + PlantUML (held for VS-D).
- No conformance rule additions (VS-CON-001..017 held for VS-D).
- No ADR-ES-003 promotion to Accepted (gated on CR-ES-003 implementation completion).
- No release tag (per v3.1.4 user directive).
- No schema migration ;;; the existing schema stub at `mappings/schema/0000-mapping.schema.json` does not match the richer shape of the existing capability mapping records ;;; held for a separate housekeeping CR.

## [0.0.1] ; 2026-09-02 ; Skeleton

### Added

- README.md (purpose, ownership, status, relationship to other repos).
- CODEOWNERS (sole owner: @emmanuel-a-otchere).
- CHANGELOG.md (this file).
- .gitignore (credential, AI-model, and workspace-noise patterns).
- LICENSE (Apache-2.0).
- Mapping schema stub at `mappings/schema/0000-mapping.schema.json`.
