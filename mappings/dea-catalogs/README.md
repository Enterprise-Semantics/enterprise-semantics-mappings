<!--
Authored by: Emmanuel A. Otchere (cardinal author rule, 2026-09-22)
Filing: CR-ES-001 §10 + §11-§13 (governance scaffolding ;;; no destructive replaces)
-->

# DEA Catalogs Mapping Boundary

This directory holds mappings between Enterprise-Semantics concepts and the DEA Catalogs (the operational catalog instances).

## Boundary (per CR-ES-001 §15 + ADR-ES-001 §4.4)

DEA Catalogs instantiate, classify, organise, and apply architectural concepts within defined catalog domains. A catalog entry shall not redefine the semantic authority of the underlying Enterprise-Semantics concept.

```text
Enterprise-Semantics
        |
        | instantiated-by
        v
OpenDEA
        |
        | classified-by
        v
DEA Catalogs
```

## Mapping record structure

Per CR-ES-001 §15. Use the same structure as `../wsf/README.md`, with `target` set to a DEA Catalog identifier (when available).

## Status

Empty at v0.0.1. First mapping records will be introduced when the DEA Catalogs require formal mapping to ES concepts (held for a future CR).

## Cardinal rules

- Author: Emmanuel A. Otchere
- D-004 dash rule
- SDO-neutral sourcing (ISO/IEC, ITU-T, ETSI, NIST)
- No vendor-specific material from embargoed sources
