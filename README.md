<h1 align="center">🩺 Obesity Levels — Exploratory Data Analysis</h1>

<p align="center">
  <em>A full statistical deep-dive into obesity trends across Mexico, Peru &amp; Colombia — from raw data to predictive modelling.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-3776AB?style=flat&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white" alt="Jupyter"/>
  <img src="https://img.shields.io/badge/pandas-Data%20Wrangling-150458?style=flat&logo=pandas&logoColor=white" alt="pandas"/>
  <img src="https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white" alt="scikit-learn"/>
  <img src="https://img.shields.io/badge/statsmodels-Stats-8B0000?style=flat" alt="statsmodels"/>
  <img src="https://img.shields.io/badge/seaborn-Viz-4C8CBF?style=flat" alt="seaborn"/>
</p>

<br>

## 📌 Overview

This project applies the **complete data-analysis pipeline** to a real-world health dataset of **2,111 individuals** and **17 attributes** — cleaning, statistics, visualization, hypothesis testing, clustering and regression — to uncover which lifestyle and physiological factors most strongly drive a person's weight.

<br>

## ✨ Key Highlights

| 🔍 Finding                                        | 📊 Result                                      |
| ------------------------------------------------- | ---------------------------------------------- |
| Strongest driver of Weight                        | **Height** (corr. 0.95)                        |
| Next strongest correlations                       | **Water intake / CH2O** (0.88), **Age** (0.79) |
| Significant categorical factors (ANOVA, p < 0.05) | **CAEC**, **CALC**, **MTRANS**                 |
| Natural clusters in the data (K-Means)            | **3 clusters**                                 |
| Best predictor set for Weight (highest R²)        | **Age, Height, FCVC, CH2O, FAF, TUE**          |

<br>

## 🛠️ Tech Stack

<table>
  <tr>
    <td><b>Data Wrangling</b></td>
    <td>pandas · NumPy — loading, cleaning, missing-value &amp; duplicate detection</td>
  </tr>
  <tr>
    <td><b>Visualization</b></td>
    <td>Matplotlib (+ 3D <code>mplot3d</code>) · seaborn — heatmaps, histograms w/ KDE, box plots, regression &amp; 3D cluster plots</td>
  </tr>
  <tr>
    <td><b>Statistics &amp; Testing</b></td>
    <td>statsmodels — OLS regression, ANOVA hypothesis testing &amp; p-value interpretation</td>
  </tr>
  <tr>
    <td><b>Machine Learning</b></td>
    <td>scikit-learn — K-Means clustering, Linear &amp; Multiple Linear Regression, train/test split, evaluation metrics</td>
  </tr>
  <tr>
    <td><b>Environment</b></td>
    <td>Python 3.10 · Jupyter Notebook</td>
  </tr>
</table>

<br>

## 🚀 Features & Methodology

The notebook is structured as a progressive EDA workflow:

- **🧹 Data Cleaning** — detecting missing values, identifying and removing redundant/duplicate observations.
- **📈 High-Level Statistics** — descriptive statistics, correlation matrix and data-distribution overviews.
- **1️⃣ Univariate Analysis** — min/max/mean, variance & standard deviation, histograms with Kernel Density Estimation, and box plots to characterize distribution and skew.
- **2️⃣ Bivariate Analysis**
  - _Linear Regression_ — numeric relationships (Weight, FCVC, NCP, FAF, TUE) segmented by Gender, family history and high-calorie food consumption.
  - _ANOVA_ — relating Weight to categorical variables (CAEC, CALC, MTRANS, NObeyesdad) via hypothesis testing.
- **3️⃣ Multivariate Analysis**
  - _K-Means Clustering_ — angle/elbow plot to choose 3 clusters, then 3D cluster visualizations across many variable combinations.
  - _Multiple Linear Regression_ — Weight predicted from every meaningful combination of 2–7 predictors, ranked by R² to find the best predictive set.
- **📝 Narrative insights** — every analysis is accompanied by markdown commentary interpreting the results, ending in an overall conclusion.

<br>

## 📂 Dataset

The dataset describes obesity levels in individuals from **Mexico, Peru and Colombia**, spanning:

- **Demographics:** Gender, Age, Height, Weight
- **Eating habits:** high-calorie food (FAVC), vegetable frequency (FCVC), main meals (NCP), snacking (CAEC), alcohol (CALC), water intake (CH2O)
- **Lifestyle:** physical activity (FAF), technology use (TUE), smoking (SMOKE), calorie monitoring (SCC), transport (MTRANS)
- **Target:** obesity classification (`NObeyesdad`)

<br>

## ⚡ Getting Started

```bash
# 1. Clone the repository
git clone https://github.com/HarshTanwar1/Obesity_Analysis.git
cd Obesity_Analysis

# 2. (Recommended) create and activate a virtual environment
python3 -m venv venv
source venv/bin/activate        # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install jupyter pandas numpy matplotlib seaborn scikit-learn statsmodels

# 4. Launch the notebook
jupyter notebook Obesity_Levels.ipynb
```

<br>

## 🎓 What I Learned

- **The full EDA pipeline** — moving methodically from raw data through cleaning, summarization, and progressively richer (uni → bi → multivariate) analysis.
- **Choosing the right tool for the relationship** — linear regression for numeric-vs-numeric vs. ANOVA for numeric-vs-categorical hypothesis testing, and how to read p-values and R².
- **Interpreting distributions** — reading histograms, KDE curves and box plots to classify skew, spread and outliers rather than just generating plots.
- **Unsupervised learning** — using the elbow/angle method to pick a sensible cluster count and visualizing K-Means results in 3D.
- **Communicating analysis** — pairing every visualization and statistic with a written interpretation so the notebook tells a coherent story.

<br>

## 🔮 Future Improvements

- **Refactor repetition into functions** — generate the dozens of near-identical regression/clustering cells programmatically with loops, drastically shrinking the notebook.
- **Reframe as classification** — predict the `NObeyesdad` target with logistic regression, decision trees or random forests, with proper train/test evaluation.
- **Stronger model validation** — report cross-validated metrics (accuracy, RMSE) instead of R² alone, and account for the dominant Height–Weight correlation.
- **Feature engineering** — derive BMI from Height & Weight and encode categorical variables consistently.
- **Interactivity** — port standout visualizations to Plotly or a small Streamlit dashboard.

<br>

---

<div align="center">

⭐ _If you found this project helpful or interesting, consider giving it a star!_ ⭐

</div>
