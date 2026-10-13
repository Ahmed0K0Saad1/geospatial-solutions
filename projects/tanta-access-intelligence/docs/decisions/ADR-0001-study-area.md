# ADR-0001: Study area is the city only (Tanta 1 + Tanta 2)

**Status:** accepted, 2026-10-12

## Context
GADM lists `Tanta` (Markaz), `Tanta 1` (Kism) and `Tanta 2` (Kism). The first is the large surrounding district, the other two are the city's own subdivisions.

## Options
1. All three records: the whole district, including the surrounding area.
2. `Tanta 1` + `Tanta 2`: the city itself.

## Decision
Option 2. The question is about urban services in the city of Tanta, so the study area should be the city.

## Consequences
- The boundary is smaller and matches the urban question.
- If the project is later extended to the district, add `Tanta` (`EGY.5.9_1`) and redo the merge.
- The selection uses `IN (...)` with exact names, so the large `Tanta` record cannot be picked up by accident.
