# Visualizing Distribution and Relationship

This folder contains the materials and code for the **Visualizing Distribution and Relationship** stage of the Index Return Analysis project, where we generate and interpret charts showing how return distributions change with holding period.

## Contents
- `assignment4.Rmd` — R Markdown source for Assignment 4: summary statistics, faceted histograms, and boxplots.
- `assignment4.pdf` — Knitted PDF output of the above.

## Goals
1. **Compute Summary Statistics**  
   Calculate mean, median, standard deviation, and percent positive/negative returns for each horizon.

2. **Visualize Distribution**  
   - Produce **faceted histograms** of 2-, 5-, and 10-year return percentages.  
   - Annotate each panel with the mean (dashed red line), median, and % positive returns.

3. **Visualize Relationship**  
   - Create a **boxplot** comparing return distributions across horizons.  
   - Use **notches** (approximate 95 % CI around the median) and a red dot for the mean.  
   - Cap the y-axis (–50 % to 300 %) to focus on the central distribution.

4. **Describe in Words**  
   - Provide prose explanations of what each chart reveals about volatility, consistency, and downside risk as holding period increases. 
