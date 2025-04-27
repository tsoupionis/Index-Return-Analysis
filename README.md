# Index-Return-Analysis

## Project Overview
This project investigates how the length of an investment horizon affects historical returns in major U.S. stock indices (Dow Jones, S&P 500, NASDAQ). By calculating 2-, 5-, and 10-year percentage returns for each index, we explore the probability and consistency of positive outcomes over different holding periods.

## Data Sources
- [**Dow Jones Industrial Average** daily closing prices](https://stooq.com/q/?s=^dji)
- [**S&P 500** daily closing prices](https://stooq.com/q/?s=^spx)
- [**NASDAQ Composite** daily closing prices](https://stooq.com/q/?s=^ndq)

All data were downloaded from Stooq.com and saved in a `data/` folder.

## Tools & Libraries
- **R** for data processing and visualization
- Libraries: **tidyverse**, **lubridate**, **knitr**, **ggplot2**

## Data Processing & Analysis Steps
1. **Date parsing:** Convert character dates to `Date` objects using `ymd()` and `mdy()`.
2. **Return calculation:** Compute 2-, 5-, and 10-year percentage returns (`(price_end/price_start – 1)*100`).
3. **Reshaping:** Combine indices and pivot into long format with a `Horizon` column.
4. **Summary statistics:** Calculate mean, median, standard deviation, and percentage of positive vs negative returns for each horizon.
5. **Visualizations:**
   - **Faceted histograms** showing distribution of returns per horizon, with mean lines and summary annotations.
   - **Boxplots** with notches (95% CI for the median) and mean markers to compare across horizons.

## Key Findings
- **Short-term (2 years):** High volatility, ~23.7% of periods yield negative returns; median ~17.2%.
- **Medium-term (5 years):** Variability declines, ~19.3% negative; median ~45.5%.
- **Long-term (10 years):** High consistency, only ~10.9% negative; median ~99.2%.

Longer holding periods not only deliver larger average gains, but also dramatically reduce the risk of loss.

## Contact
For questions or collaboration, please visit my GitHub profile or connect on LinkedIn.
