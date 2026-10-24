# Home@ix data for CADCraft

Data files only, added by Home@ix Ltd on its fork of CADCraft. No code, no binaries, no
Autodesk material. The drawings themselves stay on Google Drive; this folder holds the
index that points at them and the configurator model the index feeds.

| Folder | What it holds |
|---|---|
| `potton-library/` | Index of the Potton production drawing archive (one row per job) joined to the Ideas Book design each job is based on, with net internal areas, the Home@ix price bases and links to the Drive folders, the DWG files and the Plans and Elevations PDFs. See its README for the columns. |
| `configurator/` | The Home@ix launch configurator's data model and option list (groups, controls, options, geometry nodes, material presets, price and carbon deltas, image-generator style prompts), read from its public Strapi API on 24 October 2026, plus the natural-language configurator's architecture. |

## Why it sits in this fork

CADCraft reads and writes DXF and reads DWG (through the acadrust crate), renders to PDF,
SVG and PNG, and is drivable over MCP (`cadcraft-cli mcp`). The Home@ix configurator work
uses CADCraft as its 2D drafting and drawing-output layer: a design chosen in the
configurator is matched to a job in this index, the job's DWG files are opened with
`cadcraft-cli info` / `cadcraft-cli convert`, and plans, elevations and plot plans are
produced as DXF and PDF. IFC and 3D stay outside CADCraft (in the Python BIM agent), so no
LGPL code is read or linked here.

Upstream CADCraft (storytold/cadcraft) is not asked to carry this folder; it lives on the
`homeix/*` branches of the fork.

## Rebuilding

The index is generated from three sources: the `Potton Data Base` sheet of the Home@ix
Potton appraisal costing model, a scan of the plans-library folder on Google Drive, and
the Ideas Book index (net internal areas). Regenerate by re-running the scan and the merge
script kept with the Home@ix tooling; commit the regenerated `index.json`, `index.csv` and
`ideas-book.csv` together.

## Licence

These data files are Home@ix Ltd material and are not part of CADCraft's MIT/Apache-2.0
source. They are published on this fork for Home@ix's own use.
