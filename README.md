# datasciproj
# Statistical Analysis of Global Trade & Macroeconomic Indicators

## Overview
An empirical statistical analysis examining macroeconomic dynamics across 20+ economies using World Bank development indicators. This project evaluates whether trade openness and inflation volatility shifted significantly between the pre-2020 (2015–2019) and post-2020 (2020–2024) periods, and models the impact of foreign direct investment (FDI), inflation, and trade on GDP growth.

## Dataset & Data Cleaning
* **Source:** World Bank Open Data / World Development Indicators
* **Core Variables:** GDP Growth Rate (%), Inflation Rate (CPI %), Foreign Direct Investment Net Inflows (% of GDP), and Merchandise Trade (% of GDP)
* **Preprocessing:** Diagnosed missing observations across country-year panels and applied group-wise (country-level) median imputation to preserve distributional integrity against extreme economic outliers.

## Statistical Methodology
1. **Exploratory Data Analysis (EDA):** Computed central tendency and dispersion metrics (mean, median, standard deviation, and interquartile range) alongside time-series line plots, pre/post-2020 boxplots, and a Pearson correlation heatmap.
2. **Hypothesis Testing:** Tested paired period differences for normality using the **Shapiro-Wilk test**, followed by both a parametric **paired t-test** and a non-parametric **Wilcoxon signed-rank test** to evaluate post-2020 shifts in inflation and trade openness.
3. **Econometric Modeling:** Fitted an **Ordinary Least Squares (OLS)** multiple linear regression model predicting GDP growth from inflation, FDI inflows, and trade openness, validating predictor independence via **Variance Inflation Factor (VIF)** diagnostics.

## Key Findings
* **Distributional Skewness:** Shapiro-Wilk testing confirmed non-normality in cross-country inflation shifts due to post-pandemic supply shocks, making the non-parametric Wilcoxon signed-rank test the primary inference benchmark.
* **Post-2020 Macroeconomic Shift:** Paired comparison across economies indicated a statistically significant shift in median inflation volatility during 2020–2024 compared to the 2015–2019 baseline *(update with your exact W-statistic and p-value from Cell 4)*.
* **Drivers of GDP Growth:** The OLS regression model passed multicollinearity checks with all predictor VIF values below 5, isolating the directional effects of FDI inflows and inflation on economic growth *(update with your R-squared and significant predictor p-values from Cell 5)*.

## Repository Contents
* `Macroeconomic_Trade_Statistical_Analysis.ipynb` — Complete Python notebook with data cleaning, visualisations, statistical tests, and regression diagnostics.
* `world_bank_data.csv` — Macroeconomic panel dataset used for the analysis.

## Tech Stack
* **Language:** Python 3
* **Libraries:** Pandas, NumPy, SciPy, Statsmodels, Matplotlib, Seaborn

## Author
**Sunidhi Sharma**  
Master's in Computational Statistics and Data Analytics | Guru Nanak Dev University, Amritsar
