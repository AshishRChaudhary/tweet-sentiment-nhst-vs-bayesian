# COVID Tweet Sentiment — Statistical Analysis (Frequentist + Bayesian)

This repository contains my final project for **IST 686 (Quantitative Reasoning for Data Science, Fall 2025)** at **Syracuse University iSchool**.  
The project explores whether **tweet metadata** (e.g., word count, hashtag count, URLs, mentions, punctuation cues, user metrics) can explain variation in **tweet sentiment** (continuous polarity score).

Rather than over-focusing on “significance,” the goal is to interpret results responsibly using:
- **Frequentist regression (NHST)** + effect-size awareness  
- **Bayesian regression** + posterior uncertainty + ROPE interpretation  
- **Diagnostics** (linearity, heteroscedasticity, influence, multicollinearity, convergence via trace plots)

---

## What’s inside this repo

### ✅ Final Report
- `report/Final_Report.pdf`  
  Full write-up (EDA → modeling → diagnostics → interpretation).

### ✅ Reproducible Analysis (RMarkdown)
- `analysis/Project_Analysis.Rmd`  
  Full workflow in RMarkdown.
- `analysis/Project_Analysis.html` (or `.pdf`)  
  Knitted output for easy viewing.

### ✅ Literature / Course Reference
- `literature/` includes supporting course materials used for methodological guidance.

---

## Dataset and Source Paper (Links Only)

This repo does **not** upload the dataset file to GitHub.
I worked with the dataset locally, so **please download it from Kaggle** using the link below and update file paths in the `.Rmd` if needed.

Dataset (Kaggle):
- https://www.kaggle.com/datasets/kaushiksuresh147/covidvaccine-tweets?resource=download

Research paper using the dataset:
- https://www.tandfonline.com/doi/full/10.1080/21645515.2021.2017216

> Note: If the `.Rmd` references a local file path, replace it with your downloaded Kaggle path.

---

## Methods Summary (High-level)

### Data exploration & preparation
- Inspected univariate and bivariate distributions for skewness and non-linear patterns  
- Addressed skewed count variables using transformations when appropriate  
- Checked multicollinearity using **VIF** (kept predictors stable by removing only one from highly correlated pairs)  
- Validated modeling assumptions via diagnostics and influence checks

### Models
1. **Frequentist multiple regression (NHST)**
2. **Bayesian regression**
   - Posterior summaries, credible intervals/HDI
   - ROPE-based practical significance checks
   - Trace plots for convergence and stable sampling

### Interpretation philosophy
This project emphasizes **practical significance** and **diagnostic validity**, not just p-values, especially given large samples where tiny effects can become statistically significant.

---

## How to run (quick)
1. Download the dataset from Kaggle (link above).
2. Open `analysis/Project_Analysis.Rmd` in RStudio.
3. Update the dataset file path in the Rmd.
4. Knit the document to HTML/PDF.

---

## Credits / Acknowledgment
Course: **IST 686 – Quantitative Reasoning for Data Science (Fall 2025)**  
Instructor: **Professor Kevin Crowston**  
Student: **Ashish Chaudhary**

This project uses the same dataset referenced in the published study above; however, the analysis, diagnostics, and interpretations in this repository are my independent work for the course.

---

## Citation
If you use this repo, please cite the dataset source (Kaggle) and the original paper linked above.
