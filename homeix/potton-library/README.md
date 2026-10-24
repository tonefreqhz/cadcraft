# Potton plans library index

One row per Potton job (`index.json` → `jobs[]`, `index.csv`), plus the Ideas Book list
(`index.json` → `ideas_book[]`, `ideas-book.csv`).

Plans library root on Google Drive: the folder named in `index.json` → `sources.plans_library_root`.
Each job folder is named `10.3.<n> <job number>` and holds the production set: Plans and
Elevations PDF, slab layout DWG, panel layouts (GF/FF/SF), setting out, sole plate, head
binders, stud positions, steel beam sheets, truss layouts, joist layout, cavity barrier,
special joinery, and subfolders such as Bregs Pack, Issuing Info, Panel Elevations,
Structural, and Truss/Posi/PMR.

## Columns (`jobs[]`)

| Column | Meaning |
|---|---|
| `job` | Potton job number, `YY-NNN` (year, sequence). `18-103G` is a garage on job 18-103. |
| `client` | Client name as in the Data Base sheet. |
| `house_type_based_on` | The Potton design the job was based on, as recorded by Potton. |
| `design_note` | How the job departs from the design (mirror, plan changes, extensions). |
| `part_l_version` | Approved Document Part L edition the job was designed to. |
| `production_folder_url` | The job's full drawings production folder on Google Drive (from the Data Base sheet). |
| `production_folder_note` | Set when the Data Base sheet records no file. |
| `ideas_book_design` | The Ideas Book design matched to `house_type_based_on`. |
| `area_source` | Where `nia_ft2` comes from: the Ideas Book index, or the house-type pivot. |
| `nia_ft2`, `nia_m2` | Net internal area. |
| `list_price_230`, `turnkey_270`, `turnkey_300` | NIA × the Home@ix price bases (list £230 per sq ft; turnkey £270 and £300 per sq ft). |
| `plans_library_folder_url`, `plans_library_folder_title` | The job folder in the plans library. |
| `plans_pdf_url`, `plans_pdf_title` | The Plans and Elevations PDF in that folder. |
| `dwg_count`, `pdf_count`, `file_count`, `subfolders` | Folder contents. |
| `extracted_*` | Text read from the Plans and Elevations PDF title block, where it had a text layer. |

## Columns (`ideas_book[]`)

`design`, `nia_ft2`, `nia_m2`, `list_price_230`, `turnkey_270`, `turnkey_300`,
`jobs_in_library`, `job_numbers`, and the house-type pivot's `pivot_m2` / `pivot_ft2`
where the design appears in the pivot.

## Sources

- Home@ix Potton appraisal costing model (Google Drive copy modified 15 July 2026): Data Base sheet, house-type pivot, Ideas Book index, enquiries table.
- Plans library folder scan, 24 October 2026.
- Price bases: appraisal model (£230 per sq ft) and the customer note of 9 October 2026 (£270 to £300 per sq ft, fees 7.5 to 10 per cent).
