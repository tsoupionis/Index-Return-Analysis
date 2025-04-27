# Data Preparation and Processing

This folder contains the materials and code for the **Data Preparation and Processing** stage of the Index Return Analysis project, where we import raw price data and compute holding‐period returns.

## Contents
- `DATA-333-Midterm.Rmd` — R Markdown source for the midterm: data import, return calculations, and reshaping.  
- `DATA-333-Midterm.pdf` — Knitted PDF output of the above.

## Goals
1. **Research Question**  
   Define the probability of positive returns over 2-, 5-, and 10-year horizons.

2. **Data Source**  
   Load daily closing prices for Dow Jones, S&P 500, and NASDAQ (CSV files from `data/`).

3. **Import Data**  
   Read CSVs with `read_csv()`, parse dates (`ymd()` / `mdy()`), and preview with `head()`.

4. **Compute Dependent Variable**  
   Write `calculate_returns()` to compute percent returns over 504, 1260, and 2520 trading-day lags (~2, 5, 10 years).

5. **Define Independent Variable**  
   Use the lag columns (`Return_2yr`, `Return_5yr`, `Return_10yr`) as different `Horizon` levels.

6. **Combine & Reshape**  
   - Add an `Index` column to each data frame.  
   - `bind_rows()` to stack indices.  
   - `pivot_longer()` to create a long format with `Horizon` and `Return_pct`.

7. **Filter & Clean**  
   Remove incomplete cases (rows where return is `NA`) before analysis.

8. **Initial Summary**  
   Review the head of the processed data and confirm that `Horizon` is a factor with levels `2 Years`, `5 Years`, `10 Years`.
