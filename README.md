# KI Core Facility Usage - Data cleaning and presentation

Code in this repository assembles and cleans KI Core usage data from ilabs and external sources (if applicable).
Organized usage data is annotated with Sponsor relationships and plots are prepared.

## Purpose

The visualizations prepared here for the 2026 CCSG competivtive renewal application but the approach can be generalized for other reporting needs.
Each component of the work is executed in a separate Rmd file. The Rmd files are run in containerized Rstudio using the singularity_Rstudio_r451.sh script.

## Required supporting files

NOTE: MIT certificates are required to access these files.

KI ilabs data spanning the reporting period

- [KI ilabs report from 1/1/2020-12/31/22](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/01012020_12312022_ALL_Cores_Completed.csv)
- [KI ilabs report from 1/1/2023-10/31/25](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/01012023_10312025_ALL_Cores_Completed.csv)

Core-specific external usage data not captured in ilabs

-[Biomicrocenter external data - DSMI and IGT](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/ExtUsage2025_2510.xlsx)
-[Metabolite Profiling external - 2024 - MSBP](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/METPRO_2024_Core%20Charges%20by%20Service.xlsx)
-[Metabolite Profiling external - 2025 - MSBP](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/METPRO2025_Core%20Charges%20by%20Service.xlsx)

Lookup table between Faculty/Lab notations in the input data files and a harmonized Faculty.Key

- [Faculty Key table](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/FacultyKeys.xlsx)

Lookup table between Faculty Keys and core-specific sponsor relationships

- [Sponsorship Table](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/annotated.Faculty.Keys_tmp.xlsx)

Simplified Sponsor relationships for plotting

- [Simple Sponsors](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/sponsor.Keys.ForPlotting.xlsx)

## Clean and assembly raw ilabs data

Exported ilabs reports have a max of 3 years so to cover CCSG reporting period, 2 files are assembled. These files also have extra columns that are not used in reporting. This script and html report assembles and cleans these data and outputs a stock ilabs file used in each core script.

- [script](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/ilabs_preprocess.Rmd)
- [report](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/ilabs_preprocess.html)
- [output](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/stock_ilabs.xlsx)

## Assemble and Process data for each core

### FLOW

### MSBP

### DSMI

### TPSI

### IGT

### PMIT

### DSMI

### NanoFIB

