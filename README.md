# Clear Cut: Sustainability in Focus

## Project Overview

As conversations around climate change, ethics, and sustainability reshape the fashion industry, consumer expectations have shifted accordingly. Shoppers are more willing than ever to pay for eco-conscious and socially responsible clothing — but are fashion brands keeping up?

This repository explores that central question using **Fashion Revolution's Fashion Transparency Index** (2020–2024) and sustainability-focused **consumer sentiment data**. The project identifies top and bottom performing brands, analyzes changes in transparency scores over time, and compares industry progress against what consumers say they value.

All analysis was conducted in **Python (Google Colab)**. Visualizations were created in both **Tableau** and **Adobe Illustrator**, and are showcased on an interactive website that brings the data to life through storytelling and design.

---

## About Fashion Revolution

[**Fashion Revolution**](https://www.fashionrevolution.org/) is a global, not-for-profit movement represented by Fashion Revolution CIC with teams in over 75 countries. Born in response to the **Rana Plaza disaster** in 2013, the movement campaigns for reform in the fashion industry with a particular emphasis on **supply chain transparency**.

Each April, Fashion Revolution Week invites the public to ask brands **“Who made my clothes?”** Millions of people have participated globally since 2014.

---

## Data Sources

### Fashion Transparency Index (2020–2024)

Raw datasets were extracted from [**WikiRate**](https://wikirate.org/), an open-source platform for collaborative research on corporate sustainability. The following metrics were selected for export:

#### What the Transparency Scores Represent

The **Fashion Transparency Index score** (0–100) reflects how much information a fashion brand publicly discloses across five key areas:

1. **Policy & Commitments** – Sustainability goals, policies, and public promises  
2. **Governance** – Accountability structures, board responsibility, and oversight  
3. **Traceability** – Supplier maps, factory lists, and material sourcing disclosure  
4. **Know, Show & Fix** – Auditing, remediation, and social/environmental monitoring  
5. **Spotlight Issues** – Focus areas like climate action, wages, gender equity, and circularity  

> **Important Note:** A high transparency score does **not** guarantee that a brand is ethical or sustainable — it indicates how much the brand **shares publicly** about its practices.

All scores used in this project were averaged and analyzed to explore transparency trends across **brands**, **countries**, and **years**.

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

## Initial Visualizations

### Created in Python:
- Top/bottom company bar plots
- Boxplots for score distribution per year
- Year-over-year line chart
- Regression overlay on Transparency Index scores
- 2020 vs 2024 comparison boxplot

---

## Final Visualization Process

The final visualizations in this project were designed to communicate complex data in creative, accessible, and engaging ways. While all visuals are rooted in **code-based analysis and statistical modeling**, many were reimagined through a design-forward lens to emphasize storytelling and user interaction.

### Tableau Visualizations

- **Radial Bar Chart:**  
  Created in Tableau using brand-level average Fashion Transparency Index scores (2020–2024). Radial positions were calculated using trigonometric functions (angle-to-radian conversions), with dual `X` and `Y` coordinate calculations and a `Path Order` field to generate each bar as a line segment radiating outward from a central axis.

- **Country Map:**  
  Built in Tableau to visualize average Fashion Transparency Index scores by country for each year and across all years. Countries are shaded using a sequential color scale based on average score. A year selector enables users to track transparency changes over time.

### Illustrator Visualizations

- All remaining visualizations — including the **paper doll matching game**, **closet barrier racks**, **shopping bag timeline**, and **flat-lay grid of values** — were created in Adobe Illustrator.
- These visuals were first conceptualized from Python-based data outputs, then turned into hand-drawn or compositional images, which were **vectorized and stylized** to align with fashion and sustainability themes.
- Each visual represents findings derived directly from statistical testing and analysis (e.g., ANOVA, Tukey’s HSD, correlation matrices) and reinterpreted into a more creative and immersive visual experience.

> **Goal:** Merge rigorous data analysis with visually-driven storytelling to create a project that is both analytically grounded and aesthetically compelling.

--- 

## Interaction & Accessibility

This project was designed not just to analyze data but to make that data **engaging and intuitive** for a wider audience. Visualizations were crafted with usability in mind — emphasizing clarity, storytelling, and interactivity. The final interactive site allows users to explore insights through:

- Hover tooltips for statistical context
- Clickable icons for deeper data interpretation
- A clear visual hierarchy and accessible contrast levels

The goal is to make complex information about transparency and consumer values **approachable, explorable, and visually compelling.**

[View the Full Interactive Project Website](https://readymag.website/u1238775297/5490197/)

---

## Conclusion

This project set out to explore a central question:  
**As consumer sentiment increasingly favors sustainability, are fashion brands becoming more transparent in response?**

By analyzing five years of Fashion Transparency Index scores alongside detailed consumer survey data, the project reveals a mixed picture. While **overall transparency has improved**, and some brands have made consistent progress, the **rate and depth of change often lag behind consumer expectations**. Many of the same barriers that discourage shoppers from acting on their values — lack of visibility, trust, or clarity — persist within the brands themselves.

The creative visualizations presented here aim to bridge that gap: turning numbers into narratives, rankings into garments, and data into reflection. Whether you're an advocate, designer, or data analyst, this project invites you to **look closely at what’s being shown — and what’s still being hidden**.

> Fashion may be visual — but transparency must be visible, too.

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


