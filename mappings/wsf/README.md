<!--
Authored by: Emmanuel A. Otchere (cardinal author rule, 2026-09-22)
Filing: CR-ES-001 §10 + §11-§13 (governance scaffolding ;;; no destructive replaces)
-->

# WSF Mapping Boundary

This directory holds mappings between Enterprise-Semantics concepts and the World Semantic Foundation (WSF).

## Boundary (per CR-ES-001 §16 + ADR-ES-001 §4.1)

```text
Enterprise-Semantics
        |
        | grounded-by / specialises
        v
World Semantic Foundation
```

No WSF concept shall be copied into the Enterprise-Semantics authority merely for convenience. Where Enterprise-Semantics uses a WSF concept, the relationship shall be represented through a mapping record in this directory.

## Mapping record structure

Per CR-ES-001 §15:

```yaml
source: ES:<KIND>:<NAME>          ;; ES concept identifier
target: external:wsf:<NAME>       ;; WSF concept identifier
mapping_type: specialisation       ;; one of the 9 supported types
relationship: specialises          ;; the predicate asserted
confidence: <float 0..1>          ;; mapping confidence
status: PROPOSED                   ;; mapping lifecycle state
provenance:                       ;; provenance block
  source: ES
  research: <finding-id>
  decision: <adr-id>
  implementation: <cr-id>
  mapping: null
governing_adr: <adr-id>           ;; ADR that authorises the mapping
```

## WSF grounding classification (per FND-ES-AG-008)

Mappings from ES to WSF fall into three categories:

1. **Tier 1 Kernel Reference** ;;; ES concept references a WSF Tier 1 kernel primitive.
2. **Tier 2 Specialisation** ;;; ES concept specialises a WSF Tier 2 derived concept.
3. **ES-canonical** ;;; ES concept has no WSF equivalent ;;; no mapping record needed.

Mixed claims (one ES concept specialising multiple WSF concepts) are defects per ADR-ES-001 §4.1 and must be resolved before the mapping record can be Accepted.

## Status

Empty at v0.0.1. First mapping records will be introduced by concept-specific ADRs (ADR-ES-002 onwards).

## Cardinal rules

- Author: Emmanuel A. Otchere
- D-004 dash rule
- SDO-neutral sourcing (ISO/IEC, ITU-T, ETSI, NIST)
- No vendor-specific material from embargoed sources
