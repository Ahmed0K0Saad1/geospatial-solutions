# ADR-0004: Data files are not committed

**Status:** accepted, 2026-10-13

## Context
GADM data is free for academic and non-commercial use, and redistribution requires permission.

## Decision
Do not commit GADM files or files derived from them. Document the source, version and recreation steps instead (`data/README.md`, `docs/geo-log/`). Data folders are ignored by `.gitignore`.

## Consequences
- The repository stays small and respects the license.
- Anyone can recreate the outputs by following the log.
- Roads and services data added in stage 5 needs its own license check before anything is committed.
