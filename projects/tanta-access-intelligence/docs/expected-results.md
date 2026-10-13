# Expected results

Use this page to check your own run. Download GADM 4.1 for Egypt, follow the [geo-log](geo-log/), and compare. If a number differs, stop and find out why before going on.

| # | Check | Expected | Where it comes from |
|---|---|---|---|
| 1 | Features in `gadm41_EGY_1` | 27 (governorates) | [GEO-001](geo-log/GEO-001-study-area.md) |
| 2 | Features in `gadm41_EGY_2` | 343 | GEO-001 |
| 3 | `"NAME_1" = 'Al Gharbiyah' AND "NAME_2" LIKE 'Tanta%'` | 3 records: `Tanta` (`EGY.5.9_1`, Markaz), `Tanta 1` (`EGY.5.10_1`, Kism), `Tanta 2` (`EGY.5.11_1`, Kism) | GEO-001 |
| 4 | `"NAME_1" = 'Al Gharbiyah' AND "NAME_2" IN ('Tanta 1', 'Tanta 2')` | 2 selected | GEO-001 |
| 5 | Features after `Dissolve` (no dissolve field) | 1 | GEO-001 |
| 6 | `NAME_2` / `GID_2` in the merged layer | `Tanta 1` / `EGY.5.10_1` (values of the first record) | GEO-001, [ADR-0002](decisions/ADR-0002-dissolve.md) |
| 7 | `Check validity`, GEOS, ring self-intersection off | Valid 1, Invalid 0, Error 0 | [GEO-002](geo-log/GEO-002-validity-check.md) |
| 8 | CRS of the measurement copy | `EPSG:32636`, units metres | [GEO-003](geo-log/GEO-003-reprojection.md) |
| 9 | Extent of the measurement copy (X) | 305756 to 311253 m (tolerance 1 m) | GEO-003 |
| 10 | Extent of the measurement copy (Y) | 3405565 to 3411774 m (tolerance 1 m) | GEO-003 |
| 11 | Geometry type | Polygon (MultiPolygon), 1 feature | GEO-002, GEO-003 |

## Notes

- Extent values depend slightly on the PROJ and GDAL versions. The reference run used QGIS 4.0.3 with GDAL 3.13.0, GEOS 3.14.1 and PROJ 9.8.1.
- In stage 7 these checks become automated tests (`tests/`), so they can be run with one command instead of by eye.
