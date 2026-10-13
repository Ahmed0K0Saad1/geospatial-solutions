# QGIS files

Reusable QGIS files for this project. They contain no data and no local paths.

| File | What it is | Use |
|---|---|---|
| `tanta_study_area.qpt` | Print layout template of the study-area map (title, legend, north arrow, scale bar, frame, author, CRS and source note) | `Project > Layout Manager`, then in the "New from Template" area choose *Specific* and select this file |
| `study_boundary.qml` | Layer style of the study boundary (fill and outline) | Open the layer's `Properties > Symbology`, then `Style > Load Style...` |

## Notes

- The template and the style were created with QGIS 4.0.3.
- After loading the template, load the boundary layer first, then check the map extent and the legend entries. A layout refers to layers of the project it was made in, so it may need to be re-linked.
- The QGIS project file (`.qgz`) is not committed. It stores absolute paths of the author's computer, and the data it points to is not in the repository (see [`../data/README.md`](../data/README.md)).