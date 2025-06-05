# Index Return Analysis

This repository examines how investment horizon affects historical returns in major U.S. stock indices (Dow Jones Industrial Average, S&P 500, NASDAQ Composite). By calculating 2-, 5-, and 10-year percentage returns, visualizing distributions, conducting inferential tests, and converting to annualized returns, the project demonstrates how holding period and index choice influence return consistency and the probability of positive outcomes.

---

## Folder Structure

### 1. Data Introduction

**Purpose:** Load and inspect raw index price data; define variables.

**Contents**  
- `assignment3.Rmd` — R Markdown source for the Data-333 midterm:  
  - Loads the three CSV files (`official_dowjones_data.csv`, `official_spx_data.csv`, `official_nasdaq_data.csv`).  
  - Parses and renames columns (`Investment_Date`, `Closing_Price`).  
  - Lists variables (Date, Close) and describes dependent (`Return_pct` to be computed later) and independent variables (Time Horizon).  
- `assignment3.pdf` — Knitted PDF output of `assignment3.Rmd`.

**Goals**  
1. Load packages (`tidyverse`, `lubridate`).  
2. Import raw CSVs and preview structure.  
3. List column names and describe variables.  
4. Define the dependent variable (future Return_pct) and independent variable (Time Horizon).  
5. Rename `Date` → `Investment_Date` and `Close` → `Closing_Price`.  

---

### 2. Data Preparation and Processing

**Purpose:** Compute holding-period returns and reshape data for analysis.

**Contents**  
- `DATA-333-Midterm.Rmd` — R Markdown source for the midterm assignment:  
  - Parses dates (`ymd()`, `mdy()`), calculates 2-, 5-, and 10-year percent returns with `calculate_returns()`.  
  - Adds an `Index` column to each data frame.  
  - Combines (`bind_rows()`) and pivots to long format (`Horizon`, `Return_pct`).  
  - Filters out incomplete cases (NA returns).  
- `DATA-333-Midterm.pdf` — Knitted PDF output of `DATA-333-Midterm.Rmd`.

**Goals**  
1. State the research question: probability of positive returns over 2-, 5-, 10-year horizons.  
2. Load daily closing prices for DJI, SPX, NDQ from `data/`.  
3. Implement `calculate_returns()` to compute lagged percentage returns.  
4. Define `Horizon` using the lagged return columns.  
5. Add `Index`, `bind_rows()`, and `pivot_longer()` to create a long-format data frame with `Horizon` (2 Years, 5 Years, 10 Years) and `Return_pct`.  
6. Filter out rows with `NA` returns.  
7. Confirm that `Horizon` is a factor with the correct levels.  

---

### 3. Visualizing Distribution and Relationship

**Purpose:** Generate and interpret charts showing how return distributions change with holding period.

**Contents**  
- `assignment4.Rmd` — R Markdown source for Assignment 4:  
  1. **Compute Summary Statistics**  
     - Calculate mean, median, SD, and percent positive/negative returns for each horizon.  
  2. **Faceted Histograms**  
     - Plot 2-, 5-, 10-year return distributions.  
     - Annotate each panel with mean (dashed red line), median, and % positive returns.  
  3. **Boxplot Comparison**  
     - Create a boxplot comparing returns across horizons.  
     - Use notches (≈95 % CI around the median) and a red dot for the mean.  
     - Cap y-axis at –50 % to 300 % to focus on central distribution.  
  4. **Written Explanations**  
     - Describe what each histogram reveals about volatility and risk.  
     - Explain boxplot features and how they demonstrate holding period effects.  
- `assignment4.pdf` — Knitted PDF output of `assignment4.Rmd`.

**Goals**  
1. Compute descriptive statistics by `Horizon`.  
2. Produce faceted histograms labeled with summary metrics.  
3. Create boxplots comparing horizons (with notches and mean markers).  
4. Provide prose that explains how volatility, consistency, and downside risk change as holding period increases.  

---

### 4. Statistical Analysis and Annualized Returns

**Purpose:** Conduct ANOVAs on raw returns and calculate annualized metrics for post-1957 data, with full interpretive commentary and context versus cash alternatives.

**Contents**  
- `final_research_report.Rmd` — R Markdown source for the final report:  
  1. **Descriptive Statistics (Raw Returns)**  
     - Recompute summary tables for full vs. post-1957 data (mean, median, SD, % positive/negative).  
     - Breakdown by `Index` (Dow, S&P 500, NASDAQ).  
  2. **Visualizations (Raw Returns)**  
     - Histograms (full vs. post-1957) by horizon with annotations (Section 6).  
     - Boxplots comparing full vs. post-1957 by horizon (Section 7).  
     - Histograms by `Index` & `Horizon` (post-1957) with corner annotations (Section 8).  
     - Boxplots by `Index` & `Horizon` (post-1957) (Section 9).  
  3. **Statistical Tests**  
     - One-way ANOVAs testing mean return differences by **Horizon** on full and post-1957 datasets.  
     - One-way ANOVAs testing mean return differences by **Index** on both datasets.  
     - Section 10.1: Interpret F-statistics, degrees of freedom, and p-values (< 2 × 10⁻¹⁶).  
  4. **Annualized Return Calculations (Post-1957)**  
     - Convert multi-year returns into **annualized geometric returns**.  
     - Table 3: Annualized summary by `Horizon` (mean, median, SD, % positive/negative).  
     - Section 12.1: Interpret how volatility declines and consistency improves with longer horizons.  
     - Table 4: Annualized summary by `Index` & `Horizon`.  
     - Section 13.1: Interpret index-specific patterns (e.g., NASDAQ’s higher returns, Dow/S&P moderate).  
  5. **Takeaway & Investment Context**  
     - Section 14: Synthesize raw vs. annualized findings.  
     - Compare 10-year annualized equity returns (~ 7.97 %–10.76 %) to typical cash yields:  
       - **Certificates of Deposit (CDs):** ≈ 1 %–2 % APY  
       - **High-Yield Savings Accounts:** ≈ 3 %–4 % APY  
       - **Money Market Funds:** ≈ 4 % APY  
     - Emphasize how long-horizon equity investing historically outperforms these alternatives—critical context for younger investors.  
- `final_research_report.pdf` — Knitted PDF of `final_research_report.Rmd`.  

**Goals**  
1. Revisit summary statistics for full and post-1957 by `Horizon` and `Index`.  
2. Visualize raw return distributions (histograms, boxplots) with clear annotations and commentary.  
3. Run one-way ANOVAs for both `Horizon` and `Index` on full and filtered datasets; interpret F- and p-values.  
4. Calculate and tabulate annualized returns (post-1957) with interpretive sections (11.1, 12.1).  
5. Compare equity returns to CDs, savings accounts, and money markets in the final takeaway.  

---

## How to Navigate This Repository

1. **Data Introduction/**  
   - Open `assignment3.Rmd` to see raw data loading, variable definitions, and column renaming.  
2. **Data Preparation and Processing/**  
   - View `DATA-333-Midterm.Rmd` to understand how raw closing prices are cleaned, merged, and reshaped.  
3. **Visualizing Distribution and Relationship/**  
   - Examine `assignment4.Rmd` for histograms, boxplots, and written interpretations of raw return distributions.  
4. **Statistical Analysis and Annualized Returns/**  
   - Read `final_research_report.Rmd` to review descriptive tables, ANOVA results, annualized return summaries, and a final takeaway comparing equity vs. cash-equivalent yields.  

---

## Contact

For questions or collaboration, visit my [GitHub profile](https://github.com/tsoupionis) or connect on [LinkedIn](https://linkedin.com/in/thomas-soupionis/).  
