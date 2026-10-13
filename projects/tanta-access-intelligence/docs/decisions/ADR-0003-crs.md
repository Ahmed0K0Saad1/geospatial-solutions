# ADR-0003: Use EPSG:32636 for measurements

**Status:** accepted, 2026-10-13

## Context
Source data is EPSG:4326 (degrees). Distances and areas need metres.

## Options
1. EPSG:32636, WGS 84 / UTM zone 36N.
2. EPSG:22992, Egypt 1907 / Red Belt, a local metric system.

## Decision
Option 1. The data is already WGS 84, so no datum transformation is introduced, and zone 36N covers 30 to 36 degrees east, which includes Tanta.

## Consequences
- Options 1 and 2 are not mixed in this project.
- The EPSG:4326 boundary is kept as the reference; the UTM copy is used only for measurement.
- Reprojection is done by exporting with a new CRS, never by `Set Layer CRS`.
