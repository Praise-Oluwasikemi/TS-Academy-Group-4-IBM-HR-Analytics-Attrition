# TS-Academy-Group-4-IBM-HR-Analytics-Attrition
This repository contains an end-to-end data science pipeline.
# 📊 IBM HR Employee Attrition & Analytics Pipeline

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition/blob/main/TS_ACADAEMY_GROUP_4.ipynb)

An end-to-end data science project analyzing employee turnover (attrition) data for **1,470 employees**. This project explores key satisfaction and demographic factors driving resignations, performs unsupervised clustering, and trains predictive machine learning models to identify at-risk staff before they leave.

---

## 📌 Project Overview

This repository works through a 7-part pipeline designed for both technical and non-technical stakeholders:
1. **Data Foundation & SQL Analysis:** Automatic download of the IBM HR dataset via `kagglehub`, loaded into an in-memory SQLite database (`hr.db`) to query key departmental metrics.
2. **Feature Engineering & Encoding:** Creating domain-specific indicators and transforming categorical variables.
3. **Exploratory Data Analysis (EDA) & Clustering:** Identifying natural employee personas using K-Means and PCA dimensionality reduction.
4. **Predictive Modeling:** Training classification models to predict employee attrition based on satisfaction scores, compensation, distance from home, and tenure.

---

## 👥 Team Members (TS Academy - Group 4)

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

---

## 🛠️ Dataset & Tools Used

* **Dataset:** [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
* **Language & Libraries:** Python 3, Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn, SQLite3, KaggleHub

---

## 🚀 How to Run

### Option 1: Run Direct on Google Colab (Recommended)
Click the badge at the top of this README or click here: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition/blob/main/TS_ACADAEMY_GROUP_4.ipynb)

### Option 2: Run Locally
1. Clone this repository:
   ```bash
   git clone [https://github.com/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition.git](https://github.com/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition.git)
   cd TS-Academy-Group-4-IBM-HR-Analytics-Attrition


---

## 📋 Team Collaboration Guide (Google Colab + GitHub)

Welcome to the team! To keep our repository clean and avoid overwriting each other's work, please follow these steps whenever you work on the notebook:

### 1. Open and Work on the Notebook
1. Open our [GitHub Repository](https://github.com/Praise-Oluwasikemi/TS-Academy-Group-4-IBM-HR-Analytics-Attrition) and click the **Open in Colab** badge at the top of the README.
2. In Colab, go to **File > Save a copy in Drive**. This creates a personal copy in your Google Drive where you can test code safely without breaking the main file.

### 2. NO WORKING ON THE MAIN FILE
* **Check in on WhatsApp / Slack:** Before you start working on a section, send a quick message to the group (e.g., *"I'm working on Part 3 EDA right now"*).
* This prevents two people from working on the same part at the same time.
* Once you finished testing your code in Colab and are ready to share it with the group: paste the colab link of your personal copy.

---

### 💡 Best Practices for the Team

* **Run all cells before saving:** Make sure your code runs from top to bottom without errors
* **Keep code clear:** Add short text/markdown cells explaining what your code does so other teammates can understand your logic.
* **Never delete others' work:** If you want to modify someone else's code block, discuss it with them first.
