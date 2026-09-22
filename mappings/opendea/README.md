<!--
Authored by: Emmanuel A. Otchere (cardinal author rule, 2026-09-22)
Filing: CR-ES-001 §10 + §11-§13 (governance scaffolding ;;; no destructive replaces)
-->

# OpenDEA Mapping Boundary

This directory holds mappings between Enterprise-Semantics concepts and the OpenDEA metamodel.

## Boundary (per CR-ES-001 §17 + ADR-ES-001 §4.3)

Enterprise-Semantics concepts may be specialised or formalised by OpenDEA. An OpenDEA implementation does not redefine the semantic authority of the Enterprise-Semantics concept.

```text
Enterprise-Semantics
        |
        | specialised-by
        v
OpenDEA
        |
        | instances
        v
DEA Catalogs
```

## Mapping record structure

Per CR-ES-001 §15. Use the same structure as `../wsf/README.md`, with `target` set to an OpenDEA metamodel identifier (when available).

## No OpenDEA metamodel changes

This CR (CR-ES-001) does not include any OpenDEA metamodel changes. OpenDEA metamodel evolution is governed through OpenDEA's own CR process ;;; not through ES.

## Status

Empty at v0.0.1. First mapping records will be introduced when the OpenDEA ↔ ES boundary requires formal mapping (held for a future CR).

## Cardinal rules

- Author: Emmanuel A. Otchere
- D-004 dash rule
- SDO-neutral sourcing (ISO/IEC, ITU-T, ETSI, NIST)
- No vendor-specific material from embargoed sources
