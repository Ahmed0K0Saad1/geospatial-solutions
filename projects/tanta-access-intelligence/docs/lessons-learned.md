# Lessons learned

| What happened | Effect | What changed |
|---|---|---|
| The QGIS project was never saved (title showed `*Untitled Project`). When the computer failed, the project was lost. | The work was redone from the start. | Project saved as `tanta_project.qgz` before any layer is added; `Ctrl+S` after every step. |
| The first merge used `Dissolve coverage` instead of `Dissolve`. | All attribute fields were `NULL`. | Documented in ADR-0002; the correct tool is named in the log. |
| An export was saved as Shapefile (`.shp`) in an unplanned folder. | The file could not be found after the crash. | Outputs are GeoPackage, saved in the project data folder. |
| A layer was named `utm36n`, which says nothing about its real CRS. | A name is not proof. | The CRS is confirmed in `Properties`, `Information` and by the extent values. |
| After the merge the fields describe only `Tanta 1`. | A reader could think the boundary is one district. | Documented as a known limitation; traceable attributes kept in `tanta_1_2_admin_parts.gpkg`. |
