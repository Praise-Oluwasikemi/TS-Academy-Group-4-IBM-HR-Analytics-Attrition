# IBM HR Employee Attrition & Analytics Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition/blob/main/group_04_yourname.ipynb)

An end-to-end data science project analyzing employee turnover (attrition) data for **1,470 employees**. This project explores key satisfaction and demographic factors driving resignations, performs unsupervised clustering, and trains predictive machine learning models to identify at-risk staff before they leave.

---

## Project Overview

This repository works through a 7-part pipeline designed for both technical and non-technical stakeholders:
1. **Data Foundation & SQL Analysis:** Automatic download of the IBM HR dataset via `kagglehub`, loaded into an in-memory SQLite database (`hr.db`) to query key departmental metrics.
2. **Feature Engineering & Encoding:** Creating domain-specific indicators and transforming categorical variables.
3. **Exploratory Data Analysis (EDA) & Clustering:** Identifying natural employee personas using K-Means and PCA dimensionality reduction.
4. **Predictive Modeling:** Training classification models to predict employee attrition based on satisfaction scores, compensation, distance from home, and tenure.

---

## Team Members (TS Academy - Group 4)

* **Praise Adetayo**
* **David Wealth**
* **Michael Sampson**
* **Okogbo Joseph**
* **Vitor Oduronbi**
* **Helen Emiewo**
* **Popoola Temidayo**
* **Ogunrionola Christanah**
* **Adenmosun Bethel**
* **Dorcas Yusuf**
* **Alli Olamilekan**

---

## Dataset & Tools Used

* **Dataset:** [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
* **Language & Libraries:** Python 3, Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, SQLite3, KaggleHub

---

## How to Run

### Option 1: Run Direct on Google Colab (Recommended)
Click the badge at the top of this README or click here: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition/blob/main/group_04_yourname.ipynb)

### Option 2: Run Locally
1. Clone this repository:
   ```bash
   git clone [https://github.com/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition.git](https://github.com/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition.git)
   cd TS-Academy-Group-4-IBM-HR-Analytics-Attrition
---

# Part 2: Feature Engineering, Encoding, and Scaling
This section handles the preprocessing pipeline for the IBM HR Analytics Attrition dataset, preparing raw features into a normalized matrix for downstream clustering and classification models.

### 1. Feature Engineering
Created 3 domain-specific features to capture employee turnover drivers:
* `Income_Per_Job_Level`: Evaluates pay equity relative to job level seniority (`MonthlyIncome / JobLevel`).
* `Burnout_Risk`: Interaction term combining commute distance and overtime work (`DistanceFromHome * OverTime`).
* `Company_Tenure_Ratio`: Captures career loyalty vs. job-hopping history (`YearsAtCompany / (TotalWorkingYears + 1)`).

### 2. Categorical Encoding
* **Ordinal Encoding:** Applied to `BusinessTravel` to preserve logical progression (`Non-Travel` < `Travel_Rarely` < `Travel_Frequently`).
* **One-Hot Encoding:** Applied to nominal variables (`Department`, `EducationField`, `JobRole`, `MaritalStatus`, `Gender`, `OverTime`).
* **Multicollinearity Prevention:** Set `drop_first=True` to eliminate redundant dummy variables and avoid the dummy variable trap.


### 3. Target Variable Transformation
* Converted target `Attrition` labels into binary format (`1` for `Yes`, `0` for `No`).

### 4. Feature Scaling
* Applied `StandardScaler` across all features to standardize inputs (mean=0, variance=1) for distance-sensitive models (K-Means, Logistic Regression).

---

## Team Collaboration Guide (Google Colab + GitHub)

Welcome to the team! To keep our repository clean and avoid overwriting each other's work, please follow these steps whenever you work on the notebook:

### 1. Open and Work on the Notebook
1. Open our [GitHub Repository](https://github.com/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition) and click the **Open in Colab** badge at the top of the README.
2. In Colab, go to **File > Save a copy in Drive**. This creates a personal copy in your Google Drive where you can test code safely without breaking the main file.

### 2. NO WORKING ON THE MAIN FILE
* **Check in on WhatsApp:**
* **Create a branch for the part you are working on and make a pull request once all codes are tested**

---

### 💡 Best Practices for the Team

* **Run all cells before saving:** Make sure your code runs from top to bottom without errors
* **Keep code clear:** Add short text/markdown cells explaining what your code does so other teammates can understand your logic.
* **Never delete others' work:** If you want to modify someone else's code block, discuss it with them first.

---
