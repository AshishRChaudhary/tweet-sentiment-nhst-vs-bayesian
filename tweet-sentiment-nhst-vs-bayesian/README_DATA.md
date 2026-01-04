# Dataset Information

This project uses a publicly available dataset of COVID-19 vaccine–related tweets.
The dataset is **not included** in this repository and must be downloaded separately.

---

## Dataset Source

**Kaggle Dataset:**  
COVID Vaccine Tweets  
https://www.kaggle.com/datasets/kaushiksuresh147/covidvaccine-tweets?resource=download

---

## Why the Dataset Is Not Included

- The dataset is publicly hosted on Kaggle
- Avoids duplication and licensing concerns
- Keeps the repository lightweight and reproducible

Users should download the dataset directly from Kaggle.

---

## Expected Usage

During the original analysis, the dataset was loaded from a **local file path**.
If you are reproducing this analysis:

1. Download the dataset from Kaggle.
2. Place it anywhere on your local machine.
3. Open `analysis/Project_Analysis.Rmd`.
4. Replace the dataset file path in the data-loading section with your local path.

Example (illustrative only):
```r
tweets <- read.csv("path/to/your/covidvaccine_tweets.csv")

