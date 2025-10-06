# Exploring Environmental (In)Justice with EJScreen (EDS 223 – HW1)

> Build effective, responsible, accessible, and aesthetically pleasing maps in R using tmap while practicing vector/raster wrangling and communicating an environmental justice story.

---

## Table of contents

1. Overview
2. Repository structure
3. Data access & privacy
4. Setup
5. How to run
6. What to produce
7. Mapping requirements
8. Rubric (specifications)
9. References & acknowledgements
10. Authors
11. License

---

## 1. Overview

* Purpose: Explore an environmental justice (EJ) topic (place/issue you care about) and communicate it with two high-quality maps and a short interpretation.
* Tools: R, Quarto, tmap, sf, tidyverse.
* Deliverables: ej_screen.qmd (source) and ej_screen.pdf (rendered), plus this README. Add the repo link to the class spreadsheet.

---

## 2. Repository structure

EDS223-HW1
│  README.md
│  ej_screen.qmd
│  ej_screen.pdf
│
├─ Rmd/               (optional) scratch notebooks / project files
└─ data/
└─ ejscreen/       EJScreen inputs (NOT tracked; see .gitignore)

---

## 3. Data access & privacy

* Source: EPA EJScreen block-group data (2023). Technical docs and column dictionary are included with the data download.
* Where to put data: Unzip to data/ejscreen/ locally.
* Do not commit data: This repo ships without data. The entire data/ directory is git-ignored.

.gitignore (expected):
/data/

Docs bundled with data (review these):

* ejscreen-tech-doc-version-2-2.pdf (methods, caveats, limitations)
* EJSCREEN_2023_BG_Columns.xlsx (variable names/definitions)

---

## 4. Setup

1. Clone this repository.
2. R version: 4.3+ recommended.
3. Install packages: tidyverse, sf, tmap, here
4. Download & unzip EJScreen data → data/ejscreen/

---

## 5. How to run

1. Open ej_screen.qmd.
2. Ensure the YAML disables code folding so the PDF shows all code and outputs:

title: "Exploring Environmental (In)Justice with EJScreen"
format:
pdf:
toc: true
code-fold: false
execute:
warning: false
message: false

3. Render to PDF (via the Render button or using quarto::quarto_render("ej_screen.qmd", output_format = "pdf")).
4. Submit ej_screen.pdf to Gradescope and add your GitHub repo link to the class sheet.

---

## 6. What to produce

* Two maps that together communicate one EJ narrative (not two unrelated maps).
* One brief paragraph (3–6 sentences) interpreting what the maps show and why it matters for EJ in your chosen place/issue.

---

## 7. Mapping requirements

All maps must include:

1. Informative title.
2. Legends with clear titles and units.
3. Scale & orientation (graticules OR scale bar + north arrow).
4. Accessible color scales (logical, perceptually uniform; discrete vs. continuous appropriate to data).

Example workflow in R (adjust to your topic/area):

* Read EJScreen GDB (block groups).
* Filter to state and/or county of interest.
* Map variables with tmap (titles, legends, scale bar, compass).
* Optionally aggregate to county means.

---

## 8. Rubric (specifications)

To receive “Satisfactory”:

1. Two EJScreen maps + one cohesive paragraph that communicates an EJ issue.
2. Map elements (title, legend w/ units, scale/orientation, accessible color scale).
3. Professional document styling with all code and outputs visible (no code folding).
4. GitHub README follows MEDS guidelines; repo link added to class spreadsheet.

---

## 9. References & acknowledgements

* EPA EJScreen (2023) block-group dataset and docs:

  * Technical documentation: ejscreen-tech-doc-version-2-2.pdf
  * Column dictionary: EJSCREEN_2023_BG_Columns.xlsx
* R packages: tmap, sf, tidyverse, here.
* MEDS README Guidelines: adapted for repository-level documentation and accessibility best practices.

---

## 10. Authors

* Jackson Coldiron

---

## 11. License

* Code: MIT (recommended for reproducibility in coursework).
* Text/figures: CC BY 4.0.
* Data: Follow EPA/EJScreen terms; do not redistribute raw downloads via this repo.
