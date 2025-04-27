# Data Introduction

This folder contains the materials and code for the **Data Introduction** stage of the Index Return Analysis project, where we load and inspect the raw index price data.

## Contents
- `assignment3.Rmd` — R Markdown source for Assignment 3: importing data, listing variables, and renaming columns.
- `assignment3.pdf` — Knitted PDF output of the above.

## Goals
1. **Load Packages**: Import `tidyverse` and `lubridate` libraries.  
2. **Download Data**: Read the three CSV files (`official_dowjones_data.csv`, `official_spx_data.csv`, `official_nasdaq_data.csv`) into R.  
3. **Inspect Structure**: Show the number of rows and columns, preview the first few records.  
4. **List Variables**: Use `names()` to confirm column names (`Date`, `Close`).  
5. **Define Variables**: Describe the dependent variable (Return to be computed later) and independent variable (Time Horizon).  
6. **Rename Columns**: Rename `Date` to `Investment_Date` and `Close` to `Closing_Price` for clarity.  
7. **Verification**: Confirm renaming using `names()`.
