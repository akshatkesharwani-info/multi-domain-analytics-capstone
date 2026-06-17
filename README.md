# 🧩 Multi-Domain Analytics Capstone — Finance + Risk + Retail

![Python](https://img.shields.io/badge/Python-3.x-blue) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## Overview
A single analytics platform proving data science skills across three different business domains using three different ML techniques in one project: regression for price prediction (Finance), classification for risk prediction (Insurance/Risk), and clustering for customer segmentation (Retail) — packaged into one executive dashboard and a multi-sheet Excel report.

## Datasets
All three are built directly into Seaborn — no external downloads required: `diamonds`, `titanic`, `tips`

## Tech Stack
Python · Pandas · NumPy · Scikit-learn (Linear Regression, Random Forest, K-Means, MLPClassifier/ANN) · SciPy · Matplotlib · Seaborn · openpyxl (Excel export)

## Approach

**Domain 1 — Finance:** Predicted diamond prices with Linear Regression using carat, cut, color, clarity, depth and table.

**Domain 2 — Risk:** Predicted Titanic survival, comparing a Random Forest classifier against an ANN (MLPClassifier), plus a t-test comparing fares paid by survivors vs non-survivors.

**Domain 3 — Retail:** Segmented restaurant customers (tips dataset) into 3 groups using K-Means on bill size, tip amount, party size and tip percentage.

**Capstone packaging:** Combined all three analyses into one 6-panel executive dashboard and exported all results to a multi-sheet Excel workbook.

## Key Results & Insights
- **Diamond pricing is counter-intuitive on cut quality** — "Premium" cut diamonds average the highest price (~$4,584) while "Ideal" cut (usually considered the best) averages the lowest (~$3,457). This is a confounding effect: Ideal-cut diamonds in this dataset skew toward smaller carats, and carat dominates price far more than cut quality
- **Titanic survival drops sharply with class**: 1st class ≈65%, 2nd class ≈48%, 3rd class ≈24% — socioeconomic class was a stronger survival predictor than almost anything else
- Random Forest feature importance ranks **age** as the top survival predictor, ahead of fare and sex — a genuinely interesting counter to the popular "women and children first" narrative
- **Random Forest beat the ANN on the same Titanic task (0.854 vs 0.809 AUC)** — a good interview talking point on why tree ensembles often outperform a basic neural net on small tabular datasets
- The 3 retail segments tell a clear story: big spenders with low tip rate (~$31 bill, 14.6% tip), generous tippers on small bills (~$16 bill, 22% tip), and budget-conscious low tippers (~$16 bill, 13.7% tip) — two segments with near-identical bill size but very different tipping generosity, which is exactly the pattern K-Means picked up on

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook multi_domain_capstone.ipynb
```

## Project Structure
```
multi-domain-analytics-capstone/
├── notebooks/multi_domain_capstone.ipynb
├── reports/p20_capstone_report.xlsx
├── images/p20_capstone_dashboard.png
├── requirements.txt
└── README.md
```

## Author
Akshat Kesharwani — [LinkedIn](https://linkedin.com/in/akshat-kesharwani-b0452b346) · [Portfolio](https://akshatkesharwani-info.github.io)
