# Project overview

## The problem

Planning questions such as "is this neighbourhood well served?" are often answered with the straight-line distance between a home and a service. People do not travel in straight lines. They follow roads, and some roads are missing, one-way, or far longer than the straight line suggests.

**Tanta Access Intelligence** studies how well Tanta is served by comparing what a simple distance says with what the road network allows.

## The two levels of the project

| Level | What it covers |
|---|---|
| Geographic product | Understand the study area, prepare and validate Tanta's data, analyse distances or road-based access, and produce an explainable map and report |
| Software engineering product | Turn repeated steps into Python, write tests, organise files, document how to run it, use Git; consider SQL, PostGIS or an API only if the project really needs them |

The first level builds understanding of the problem and of spatial data. The second turns that understanding into something that can be re-run and maintained.

## Why QGIS first, Python later

| Tool | Role |
|---|---|
| QGIS | Explore and inspect: see the boundary, test geometry validity, spot overlaps and CRS problems. Spatial errors often do not show up in code or in a table of numbers. |
| Python + GeoPandas | Automate: once data and logic are settled, read the files, run the analysis and export results without manual clicks, so it can be re-run on updated data and tested. |
| SQL + PostGIS | Store and query: only when the data needs managing in a database that an application will use. |

Writing code first would mean building on unchecked assumptions. The plan is to get one correct analysis on real data in QGIS, then convert that part to Python and compare the results.

## Key concept: straight line versus real access

A shortest geometric distance is easy to compute and often misleading. Accessibility depends on the road network. Stage 2 (engineering thinking) turns this difference into concrete questions that the later stages answer with data.
