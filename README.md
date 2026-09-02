# enterprise-semantics-mappings

> Enterprise-Semantics bi-directional mappings: ES to WSF, ES to OpenDEA, ES to DEA Catalogs. Mapping assertions, not copies.

This repository holds **governed bi-directional mappings** between Enterprise-Semantics and the systems it integrates with: WSF (upstream), OpenDEA (downstream), DEA Catalogs (downstream instances).

A mapping is a governed assertion, not a copy. Each mapping carries:

- Source concept identifier
- Target concept identifier
- Direction (forward or inverse)
- Predicate (`grounded-by`, `aligned-with`, `specializes`, `references`, `maps-to`, `represented-by`, `profile-of`)
- Status (`proposed`, `investigating`, `established`)
- Provenance and rationale

## Status

**Skeleton (v0.0.1).** First mapping skeletons land in Phase 4.6.

## Mapping schema (stub)

The stub schema lives at [`mappings/schema/0000-mapping.schema.json`](mappings/schema/0000-mapping.schema.json). It will gain fields as the first real mappings are added.

## Planned mappings

- `wsf/` ;;; ES to WSF (`grounded-by`, `aligned-with`, `specializes`, `references`).
- `opendea/` ;;; ES to OpenDEA (`maps-to`, `represented-by`, `specializes`, `profile-of`).
- `dea-catalogs/` ;;; ES to DEA Catalogs (instance-level mappings).

## Relationship to other repositories

| Repository | Relationship |
|------------|--------------|
| [`enterprise-semantics`](https://github.com/Enterprise-Semantics/enterprise-semantics) | Source: mappings reference concept IDs from this repository. |
| [`enterprise-semantics-spec`](https://github.com/Enterprise-Semantics/enterprise-semantics-spec) | Spec: mapping schema and predicate vocabulary are specified here. |
| [`enterprise-semantics-test-probe`](https://github.com/Enterprise-Semantics/enterprise-semantics-test-probe) | Conformance: mapping integrity is validated. |

## License

Apache License 2.0. See [LICENSE](https://github.com/Enterprise-Semantics/enterprise-semantics-mappings/blob/main/LICENSE).
