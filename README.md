# geospatial-solutions

Real-world geospatial software engineering projects. Building production-ready solutions for location intelligence, site selection, and spatial analysis.

## Projects

| Project | What it answers | Status |
|---|---|---|
| [Tanta Access Intelligence](projects/tanta-access-intelligence/) | How well do residents of Tanta, Egypt, actually reach urban services through the road network? | In progress: study area prepared and validated, data collection is next |

## How this repository is organised

Each project lives in its own folder under `projects/` and follows the same layout:

```
projects/
└── tanta-access-intelligence/
    ├── README.md
    ├── docs/
    ├── data/
    ├── qgis/
    ├── src/
    └── tests/
```

## Working principles

- **Prove it in QGIS, then automate it in Python.** No code is written on top of an assumption that has not been checked on real data.
- **Every step is logged** with its goal, the reason for it, the result, and the evidence.
- **Every important choice is recorded** as a short decision record, including the options that were rejected.
- **Honest status.** A stage is marked done only when its output exists and has been checked.

## License

MIT. Third-party data used by a project keeps its own license; see each project's `data/README.md`.
