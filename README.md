# Investigating the Legacy of Redlining in Los Angeles

## Purpose

This repository contains a geospatial analysis investigating how 1930s redlining practices by the Home Owners' Loan Corporation (HOLC) continue to influence current environmental justice conditions and biodiversity observations in Los Angeles County. The analysis examines:

- Environmental and socioeconomic disparities across historically redlined neighborhoods
- Patterns in citizen science bird observations relative to historical HOLC grades
- The persistent impacts of discriminatory housing policies on community health and environmental quality

This project was completed as part of EDS 223: Spatial Analysis at the Bren School of Environmental Science & Management, UC Santa Barbara.

## Repository Structure

```
EDS223-HW2/
│
├── data/                          # Data directory (not tracked in git)
│   ├── ejscreen/                  # EPA EJScreen census block group data
│   ├── mapping-inequality/        # Historical HOLC redlining boundaries
│   └── gbif-birds-LA/            # Bird observation data from GBIF
│
├── EDS223-HW2.qmd                # Main analysis Quarto document
├── EDS223-HW2.pdf                # Rendered analysis report
├── .gitignore                    # Git ignore file (excludes data/)
└── README.md                     # This file
```

## Data Access

Due to file size constraints, the data used in this analysis is not included in this repository but can be accessed from the following sources:

1. **EJScreen Data**: EPA's environmental justice screening tool providing census block group-level data
   - Download from: [EPA EJScreen](https://www.epa.gov/ejscreen)
   - File: `EJSCREEN_2023_BG_StatePct_with_AS_CNMI_GU_VI.gdb`

2. **Historical Redlining Data**: HOLC neighborhood boundaries and grades for Los Angeles
   - Download from: [Mapping Inequality](https://dsl.richmond.edu/panorama/redlining/)
   - File: `mapping-inequality-los-angeles.json`

3. **Bird Observations**: Citizen science bird observations from Los Angeles County (2021-2023)
   - Download from: [GBIF](https://www.gbif.org/)
   - File: `gbif-birds-LA.shp`

After downloading, place all data files in a `data/` directory following the structure shown above.

## Running the Analysis

### Required R Packages

```r
library(tidyverse)   # Data wrangling
library(sf)          # Spatial data handling
library(here)        # File path management
library(tmap)        # Mapping
library(ggplot2)     # Visualization
library(gt)          # Tables
library(viridis)     # Color palettes
```

### Instructions

1. Clone this repository
2. Download the required data files (see Data Access section)
3. Place data files in the `data/` directory
4. Open `EDS223-HW2.Rproj` in RStudio
5. Render `EDS223-HW2.qmd` to generate the PDF report

## Author

**Garrett Craig**
Master of Environmental Data Science
Bren School of Environmental Science & Management, UC Santa Barbara

## References & Acknowledgments

### Data Sources

- **U.S. Environmental Protection Agency.** (2023). *EJScreen: Environmental Justice Screening and Mapping Tool* (Version 2023). Retrieved from https://www.epa.gov/ejscreen

- **Digital Scholarship Lab, University of Richmond.** *Mapping Inequality: Redlining in New Deal America*. Retrieved from https://dsl.richmond.edu/panorama/redlining/

- **Global Biodiversity Information Facility (GBIF).** Bird observations for Los Angeles County, 2021-2023.

### Key Literature

- Ellis-Soto, D., Chapman, M., & Locke, D. H. (2023). Historical redlining is associated with increasing geographical disparities in bird biodiversity sampling in the United States. *Nature Human Behaviour*, 7, 1869–1877. https://doi.org/10.1038/s41562-023-01688-5

### Course

This analysis was completed as Homework Assignment 2 for EDS 223: Spatial Analysis, taught by Professor Ruth Oliver at the Bren School of Environmental Science & Management.

## License

This project is part of academic coursework and is intended for educational purposes.
