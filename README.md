# Clear Cut: Fashion Transparency in Focus

## Project Overview

This repository explores trends in fashion industry transparency using **Fashion Revolution's Fashion Transparency Index** from 2020 to 2024. The analysis identifies top and bottom performers, tracks changes in average scores across years, and compares industry progress with **consumer sentiment data**. All analysis was performed using **Python (Colab)**, with final visuals created in **Tableau**.

---

## About Fashion Revolution

[**Fashion Revolution**](https://www.fashionrevolution.org/) is a global, not-for-profit movement represented by Fashion Revolution CIC with teams in over 75 countries. Born in response to the **Rana Plaza disaster** in 2013, the movement campaigns for reform in the fashion industry with a particular emphasis on **supply chain transparency**.

Each April, Fashion Revolution Week invites the public to ask brands **“Who made my clothes?”** Millions of people have participated globally since 2014.

---

## Data Sources

### Fashion Transparency Index (2020–2024)

Raw datasets were extracted from [**WikiRate**](https://wikirate.org/), an open-source platform for collaborative research on corporate sustainability. The following metrics were selected for export:

- **2020–2023 Metrics:**
  - Policy & Commitments Score
  - Governance Score
  - Know, Show & Fix Score
  - Traceability Score
  - Spotlight Issues Score
  - Fashion Transparency Index

- **2024 Expanded Metrics:**
  - Accountability Score
  - Decarbonisation Score
  - Energy Procurement Score
  - Financing Decarbonisation Score
  - Just Transition and Advocacy Score
  - Traceability Score
  - Fashion Transparency Index

Each dataset included:
- Company
- Year
- All metrics above
- Country (manually added using WikiRate)

#### Data Cleaning Process:
- Raw exports had **metrics in rows**, with each company listed multiple times.
- Converted to **wide format** (one row per company, one column per metric).
- Removed duplicates and reshaped data.
- Added `Country` column for Tableau use.
- Final datasets saved as `.csv` and analyzed using Python.

---

### Consumer Sentiment Dataset

Sourced from the **National Institute of Health (NIH)** and attributed to:

- **Annarita Colasante**
- **Idiano D'Adamo**

#### About the Dataset:
- Surveyed 402 participants on sustainable apparel behavior.
- 89-question instrument measured:
  - Willingness to pay for sustainable features
  - Barriers to secondhand clothing
  - Environmental values
- Anonymized (only age, gender, income, region, education retained)
- Data was originally cleaned and analyzed in R, then reformatted in Python for this project.

---

## Methodology

### 1. Top & Bottom Companies by Metric
Each year, the **top 5 and bottom 5 companies** were identified per metric. These were visualized using horizontal bar charts.

### 2. Metric Averages by Year
For every metric and year, we calculated and visualized the **average score**, giving a snapshot of industry-wide performance.

### 3. One-Way ANOVA
We used a one-way **ANOVA test** to determine if the **average Transparency Index** scores varied significantly by year.

- **Result:** p = 0.00099 (significant)
- **Conclusion:** Transparency scores **did change significantly** over time.

### 4. Tukey HSD Post-Hoc Test
Tukey’s test compared each pair of years to pinpoint which ones were different.

- **2020 vs 2023** and **2020 vs 2024** showed **statistically significant improvements**.

### 5. Linear Regression
A simple regression modeled the trend in **average Transparency Index scores** over time.

- **Positive slope** suggests upward trend
- **R² = 0.15** → modest model strength
- Not statistically significant (likely due to small sample size), but visually compelling

---

## Visualizations

### Created in Python:
- Top/bottom company bar plots
- Boxplots for score distribution per year
- Year-over-year line chart
- Regression overlay on Transparency Index scores
- 2020 vs 2024 comparison boxplot

### Created in Tableau: (link will eventually be here with more info)
- Country average map
- Transparency Index change over time
- Top/bottom filters
- Integrated comparison with consumer sentiment

---

## Purpose of This Project

This project aims to provide a data-driven view of how transparency in the fashion industry has evolved. It connects **brand behavior** with **consumer expectations**, making the case for continued accountability, disclosure, and reform.

The work here can support:
- Academic research
- Sustainability reporting
- Data journalism
- Public awareness campaigns

---

## Citations & Credits

### Fashion Transparency Index (2020–2024)  
> Fashion Revolution. Fashion Transparency Index (2020–2024). Data retrieved from [https://wikirate.org](https://wikirate.org)

### Consumer Behavior Dataset  
> Colasante, A. & D'Adamo, I. (2022). *Sustainability and Consumer Behavior in the Apparel Sector*. NIH Open Dataset.

### Data Collection and Analysis  
Data cleaning, formatting, and all Python-based analysis performed by Scarlett Moldovan. Visuals were used to inform the final Tableau dashboard.

---

## Tools Used
- Python (Google Colab)
- pandas, seaborn, matplotlib, scipy, statsmodels
- Tableau Public

---


