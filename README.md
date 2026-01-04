# COVID Tweet Sentiment - Statistical Analysis (Frequentist & Bayesian)

The project investigates whether **tweet metadata** (e.g., word count, hashtags, URLs, mentions, punctuation cues, and user-level metrics) meaningfully explains variation in **tweet sentiment** related to COVID-19 vaccination. The emphasis is on **statistical inference, diagnostics, and responsible interpretation**, rather than predictive performance alone.

---

## Results at a Glance
- Metadata-based models showed limited explanatory power for sentiment, reinforcing the need for careful interpretation beyond statistical significance.
- Model diagnostics (collinearity, residual behavior, influence checks, and convergence) played a central role in guiding conclusions.
- Frequentist and Bayesian analyses were directionally consistent, despite overall weak effect sizes.

---
## Repository Contents

### 📘 Final Report
- `report/Final_Report.pdf`  
  Complete written report covering:
  - Research questions and data understanding  
  - Data exploration and preparation  
  - Frequentist and Bayesian analyses  
  - Model diagnostics  
  - Interpretation and conclusions  

### 📊 Reproducible Analysis
- `analysis/Project_Analysis.Rmd`  
  Full RMarkdown workflow used for analysis.
- `analysis/Project_Analysis.html` (or `.pdf`)  
  Knitted output for easy review of results, tables, and diagnostics.

### 📚 Literature
- `literature/`  
  Contains course-related reference material used for conceptual and methodological guidance.

### 🗂 Data Instructions
- `README_DATA.md`  
  Explains where to obtain the dataset and how to connect it to the analysis.
  (No raw data files are stored in this repository.)

---

## Tech Stack

- `R` , `RMarkdown`
- `tidyverse` (data manipulation and visualization)
- `performance` (VIF and diagnostic checks)
- Bayesian modeling packages (for posterior estimation and convergence diagnostics)

## Dataset and Source Paper

This project uses a publicly available dataset but does **not** upload the data to GitHub.

### Dataset (Kaggle)
https://www.kaggle.com/datasets/kaushiksuresh147/covidvaccine-tweets?resource=download

### Research Paper Using the Dataset
Kalin, M., Rohani, P., & Kumar, S. (2022). *Forecasting the COVID-19 vaccine uptake rate: An infodemiological study in the US*.  
https://www.tandfonline.com/doi/full/10.1080/21645515.2021.2017216

> Note: The dataset was loaded locally during analysis. Users cloning this repo should download the dataset from Kaggle and update file paths in the RMarkdown file accordingly.

---

## Methods Overview (High-Level)

### Data Exploration & Preparation
- Examined univariate and bivariate distributions for skewness and non-linearity  
- Applied transformations where appropriate for skewed count variables  
- Evaluated multicollinearity using **VIF**  
- Assessed assumptions through residual diagnostics and influence measures  

### Statistical Models
1. **Frequentist multiple linear regression (NHST)**
2. **Bayesian regression**
   - Posterior summaries and uncertainty
   - ROPE-based practical significance
   - Trace plots for convergence assessment

The analysis prioritizes **effect sizes, uncertainty, and diagnostics**, especially given the large sample size.

---

## How to Run the Analysis

1. Download the dataset from Kaggle (link above).
2. Open `analysis/Project_Analysis.Rmd` in RStudio.
3. Replace the local dataset file path with your own.
4. Knit the document to HTML or PDF.

---

## Credits and Acknowledgment

- **Course:** IST 686 – Quantitative Reasoning for Data Science (Fall 2025)  
- **Instructor:** Professor Kevin Crowston  
- **Student:** Ashish Chaudhary  

While this project is based on the same dataset examined in Kalin et al. (2022) and informed by their conceptual approach, the analytical methods, diagnostics, and interpretations presented here represent my independent work for this academic learning.

---

## Citation

If you reference this repository, please cite:
- The Kaggle dataset (link above)
- Kalin et al. (2022), *Human Vaccines & Immunotherapeutics*
