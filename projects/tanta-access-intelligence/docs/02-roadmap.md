# Roadmap

Green means the core of the stage is done, not that every final requirement is finished.

| # | Stage | Status | Evidence |
|---|---|---|---|
| 1 | Business problem | Initial | Tanta chosen; first idea: relation between roads and services |
| 2 | Engineering thinking | In progress | Straight-line distance versus real access |
| 3 | GIS model and study area | Done | `tanta_1_2_admin_parts.gpkg`, `tanta_study_boundary.gpkg` ([GEO-001](geo-log/GEO-001-study-area.md)) |
| 4 | Data quality and CRS | Done | Validity 1/0/0 ([GEO-002](geo-log/GEO-002-validity-check.md)); EPSG:32636 copy ([GEO-003](geo-log/GEO-003-reprojection.md)) |
| 5 | Roads and services data | Next | Collect roads and services, assess coverage and credibility |
| 6 | Spatial logic | Not started | Choose suitable distances, verify results |
| 7 | Python automation | Not started | Reproducible, tested workflow |
| 8 | Testing and portfolio | Not started | Test documentation, results, publication |

## Next step: stage 5

Before downloading anything, decide:

1. Which services are measured (for example health, education, markets)?
2. Where does the road data come from, how complete is it for Tanta, and how will that be checked?
3. What does a service need to have to count (location accuracy, opening status)?

The quality of the roads and services data will limit how far the later analysis can be trusted.
