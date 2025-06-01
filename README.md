# Elevate-Labs-AI-ML-Internship-Task-2
This repository explores the Titanic dataset through visualizations and statistics to uncover patterns, trends, and insights. It includes univariate, bivariate, and correlation analyses with detailed observations.

# Task 2: Exploratory Data Analysis (EDA)

## Objective
Perform thorough exploratory analysis on the Titanic dataset to uncover:
- Descriptive statistics  
- Univariate distributions (histograms, boxplots)  
- Bivariate relationships (survival vs. features)  
- Pairwise feature relationships (pairplots, correlation matrix)  
- Key patterns, trends, anomalies, and actionable inferences  

## Dataset
- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/datasets/yasserh/titanic-dataset)  
- Or loaded via Seaborn’s built-in example.

## Libraries / Tools
- Python 3.x  
- pandas, numpy  
- matplotlib, seaborn  

---

## Steps Performed

1. **Imports & Data Loading**  
   - Loaded the Titanic dataset using Seaborn or CSV  
2. **Initial Inspection**  
   - Inspected dataset using `head()`, `tail()`, `shape`, and `info()`  
3. **Summary Statistics**  
   - Used `describe()` for numeric columns  
   - Counted unique values and mode for categorical columns  
4. **Missing Value & Unique Value Examination**  
   - Identified columns with missing values  
   - Examined categorical features for unique values  
5. **Univariate Analysis**  
   - Histograms and boxplots for `age`, `fare`, `sibsp`, `parch`, etc.  
   - Detected skewed distributions and outliers  
6. **Bivariate Analysis**  
   - Survival rate by gender (`sex`)  
   - Survival rate by class (`pclass`)  
   - Comparison of survival against fare, age, and family size  
7. **Pairplot & Correlation Matrix**  
   - Pairwise relationships across key numeric features  
   - Heatmap showing correlation between variables  

---

## 🔍 Key Observations & Patterns

### 📊 1. **Gender Disparity in Survival**
- **Female survival rate:** ~74%  
- **Male survival rate:** ~19%  
- Strong evidence of the "women and children first" policy in effect.

### 💰 2. **Class Disparity**
- **1st Class:** ~63% survived  
- **2nd Class:** ~47% survived  
- **3rd Class:** ~24% survived  
- Higher-class passengers had better access to lifeboats and crew assistance.

### 🧒 3. **Age Distribution**
- Most passengers were between **20–40 years old**.  
- A small number of infants and elderly passengers were on board.  
- Median age: ~28  
- Age missing in ~20% of entries.

### 🎟 4. **Fare Distribution**
- Highly **right-skewed**; majority paid < $50.  
- Few passengers paid very high fares (~$500).  
- Passengers who paid higher fares tended to be in 1st class and had higher survival chances.

### 👨‍👩‍👧 5. **Family Size vs. Survival**
- Passengers traveling **with family (family size = 2 to 4)** had a **higher chance of survival**.  
- Those **traveling alone** or in **very large families (6+)** had **lower survival rates**.

---

## 🔗 Correlation Matrix Insights

| Feature Pair      | Correlation | Interpretation                                   |
|------------------|-------------|--------------------------------------------------|
| `survived` & `sex`    | ≈ **+0.54**   | Strong positive correlation (female more likely to survive) |
| `survived` & `pclass` | ≈ **−0.34**   | Higher class → higher survival rate              |
| `survived` & `fare`   | ≈ **+0.26**   | Expensive ticket → more likely to survive        |
| `sibsp` & `parch`     | ≈ **+0.41**   | Passengers with siblings often had parents too   |

---

## 📌 Inferences & Recommendations

1. **Gender and class** are the strongest survival predictors.  
2. **Fare** is a good proxy for class and wealth; useful for modeling but potentially collinear with `pclass`.  
3. **Age** shows some effect (children slightly favored), but needs careful imputation before modeling.  
4. **Family size** is a potential engineered feature worth including.  
5. **Data preprocessing** should include handling missing `age`, encoding `sex`/`embarked`, and removing outliers in `fare`.

---

## How to Reproduce

1. Clone this repo.  
2. Open `task2_notebook.ipynb` in Jupyter Notebook.  
3. Run each cell sequentially to view all plots and written observations.  

---
