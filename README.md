# Part 2: Feature Engineering, Encoding, and Scaling

This section handles the preprocessing pipeline for the IBM HR Analytics Attrition dataset, preparing raw features into a normalized matrix for downstream clustering and classification models.

## Key Implementation Steps

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

## Output Artifacts
* `X_scaled_df`: Processed and scaled feature matrix ready for modeling.
* `y`: Binary target vector for classification tasks.
