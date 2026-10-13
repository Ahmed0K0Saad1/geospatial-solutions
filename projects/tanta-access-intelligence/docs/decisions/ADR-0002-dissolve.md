# ADR-0002: Use Dissolve, not Dissolve coverage

**Status:** accepted, 2026-10-12

## Context
Two QGIS tools have similar names: `Dissolve` (Vector geometry) and `Dissolve coverage` (Vector coverage).

## What happened
The first attempt used `Dissolve coverage`. The shape merged, but every attribute field of the result was `NULL`. Re-running with `Dissolve` kept field values from the first record.

## Decision
Use `Dissolve` (Vector geometry). Keep the unmerged `tanta_1_2_admin_parts.gpkg` so no administrative information is lost.

## Consequences
- The merged layer's fields describe `Tanta 1` only. This is documented in the README and in GEO-001.
- If attributes that describe both districts are needed, use `Aggregate` with concatenation, or edit the fields on purpose and document it.
