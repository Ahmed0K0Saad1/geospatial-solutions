# Data notes

Data files are **not committed** (see `.gitignore`). This page explains where they come from, how to check you have the same input, and where to put them.

## Source

| Item | Value |
|---|---|
| Dataset | GADM administrative boundaries |
| Version | 4.1 |
| Download | https://gadm.org/download_country.html (Egypt, Shapefile) |
| Files used | `gadm41_EGY_1.shp` (27 governorates), `gadm41_EGY_2.shp` (343 level-2 units) |
| License | Free for academic and non-commercial use; redistribution needs permission from GADM |

As far as the GADM site shows, 4.1 is the current version (released July 2022). Check the download page for newer versions before starting fresh work.

## Check that you have the same input

Compute the SHA-256 of the downloaded zip and compare it with the one recorded here.

```
Windows (Command Prompt):  certutil -hashfile gadm41_EGY_shp.zip SHA256
Linux / macOS:             sha256sum gadm41_EGY_shp.zip
```

Reference value for `gadm41_EGY_shp.zip`: `39fbca8fe5e1c4daeb05b2b7c000e5ba989ac2f0039b0ca10238d9f4319c81e9`

A different hash does not prove an error, but it means the input differs and the results must be compared with care.

## Where to put the files

Paths are relative to this project folder. Nothing inside `raw/` or `processed/` is committed.

```
data/
├── raw/
│   └── gadm41_EGY_shp/            unzipped GADM download
│       ├── gadm41_EGY_1.shp       (with .shx, .dbf, .prj, .cpg)
│       └── gadm41_EGY_2.shp       (with .shx, .dbf, .prj, .cpg)
└── processed/
    ├── tanta_1_2_admin_parts.gpkg
    ├── tanta_study_boundary.gpkg
    └── tanta_study_boundary_utm36n.gpkg
```

## How to recreate the outputs

Follow [`docs/geo-log/`](../docs/geo-log/) in order: GEO-001, GEO-002, GEO-003. Then compare with [`docs/expected-results.md`](../docs/expected-results.md).

## Output summary

| File | CRS | Features | Notes |
|---|---|---|---|
| `tanta_1_2_admin_parts.gpkg` | EPSG:4326 | 2 | `Tanta 1` (`EGY.5.10_1`) and `Tanta 2` (`EGY.5.11_1`), type Kism, all original fields |
| `tanta_study_boundary.gpkg` | EPSG:4326 | 1 | Dissolve result; attributes come from the first record |
| `tanta_study_boundary_utm36n.gpkg` | EPSG:32636 | 1 | bounding box X 305756 to 311253 m, Y 3405565 to 3411774 m |
