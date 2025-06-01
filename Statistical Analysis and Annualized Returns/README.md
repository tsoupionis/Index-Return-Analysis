# Statistical Analysis and Annualized Returns

This folder contains the materials and code for the **Statistical Analysis and Annualized Returns** stage of the Index Return Analysis project, where we perform inferential tests on return distributions and calculate annualized metrics for post-1957 data.

## Contents
- `final_research_report.Rmd` — R Markdown source for the final report: descriptive statistics, visualizations, ANOVA tests, and annualized return calculations.
- `final_research_report.pdf` — Knitted PDF output of the above.

## Goals
1. **Compute Summary Statistics**  
   - Revisit mean, median, standard deviation, and percent positive/negative returns for each 2-, 5-, and 10-year horizon (full and post-1957 datasets).  
   - Break down summary statistics by index (Dow Jones, S&P 500, NASDAQ) and horizon.

2. **Visualize Distributions**  
   - Generate **faceted histograms** showing raw return distributions for each horizon (full vs. post-1957).  
   - Annotate each histogram panel with mean (dashed red line), median, and % positive returns.  
   - Create **index-by-horizon histograms** for post-1957 data, highlighting how each index’s distribution shifts.

3. **Visualize Relationships**  
   - Produce **boxplots** comparing return distributions across horizons and scenarios (full vs. post-1957), using notches for 95 % CI around medians and red dots for means.  
   - Generate **boxplots by index** (post-1957) to illustrate how volatility and central tendency change with horizon for each index.

4. **Conduct Statistical Tests**  
   - Perform one-way **ANOVAs** to test for significant differences in mean returns by **Horizon** (2, 5, 10 years) and by **Index** (Dow, S&P 500, NASDAQ) on both full and post-1957 datasets.  
   - Summarize F-statistics, degrees of freedom, and p-values, and interpret results in context.

5. **Calculate Annualized Returns**  
   - Convert multi-year cumulative returns into **annualized geometric returns** for post-1957 horizons.  
   - Tabulate annualized metrics (mean, median, SD, % positive/negative) by horizon and by index.

6. **Interpret Findings and Contextualize**  
   - Provide inline commentary for every table and figure, explaining what each output reveals about volatility, risk, and return consistency.  
   - Compare long-term equity returns to typical cash-equivalent rates (CDs, high-yield savings, money markets) to highlight implications for younger investors seeking growth.

7. **Deliver Final Takeaway**  
   - Synthesize results to underscore how holding period and index choice affect outcomes.  
   - Emphasize the historical advantage of long-horizon equity investing versus traditional savings vehicles.
