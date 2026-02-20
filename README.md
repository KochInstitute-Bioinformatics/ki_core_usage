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

Lookup table between Faculty/Lab notations in the raw input data files and a harmonized Faculty.Key

```{text}
NOTE: This table contains Faculty/Lab notations from the 1/1/00-10/31/25 ilabs data, metpro external and bmc external data. 
If new ilabs or external data are added, we must check for new Faculty/Lab notations and annotate any new ones to a key in the format "Last, First". 
Each individual should have only one key and that key should exactly match the key in sponsor annotation table.
```

- [Faculty Key table](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/FacultyKeys.xlsx)

Lookup table between Faculty Keys, faculty annotations such as KI affiliation and program, and core-specific sponsor relationships
```{text}
NOTE: Different cores can have different sponsorship relationships with faculty members. 
IGT and DSMI are identical so these are combined. MSB has 2 sub-cores (metpro and biopolymers) so this core has 2 columns.
```

- [Sponsorship Table](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/annotated.Faculty.Keys_tmp.xlsx)

Simplified Sponsor relationships for plotting

- [Simple Sponsors](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/sponsor.Keys.ForPlotting.xlsx)

## Clean and assemble raw ilabs data

Exported ilabs reports have a max of 3 years so to cover CCSG reporting period, 2 files are assembled. These files also have extra columns that are not used in reporting. This script and html report assembles and cleans these data and outputs a stock ilabs file used in each core script.

- [script](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/ilabs_preprocess.Rmd)
- [report](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/ilabs_preprocess.html)
- [output](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/data/stock_ilabs.xlsx)

## Assemble and Process data for each core

For each core, there are 4 steps in the processing:

1 - Preparation of a script that extracts data from the stock ilabs file, and applicable, adds external data.
    The script annotates the data with sponsorship information and prepares visualizations
2 - Preparation of html report from script
3 - Export final data file in excel format
4 - Prepare the pie chart panel for the CCSG application. This figure may need adjustments in illustrator.

### FLOW

- [script](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/Flow_Processing.Rmd)
- [report](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/Flow_Processing.html)
- [data_file](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/flow.final.xlsx)
- [figure](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/figures/Flow_combo.pie.pdf)

### MSBP

- [script](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/MSBP_Processing.Rmd)
- [report](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/MSBP_Processing.html)
- [data_file](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/msbp.final.xlsx)
- [figure](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/figures/MSBP_combo.pie.pdf)

### DSMI

- [script](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/DSMI_processing.Rmd)
- [report](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/DSMI_processing.html)
- [data_file](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/dsmi.final.xlsx)
- [figure](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/figures/DSMI_combo.pie.pdf)

### TPSI

- [script](https://bmc-data.mit.edu/BCC/cw.lab3/KI_core_usage/analysis/TPSI_processing.Rmd)
- [report]()
- [data_file]()
- [figure]()

### IGT

- [script]()
- [report]()
- [data_file]()
- [figure]()

### PMIT

- [script]()
- [report]()
- [data_file]()
- [figure]()

### HTS

- [script]()
- [report]()
- [data_file]()
- [figure]()

### NanoFIB

- [script]()
- [report]()
- [data_file]()
- [figure]()