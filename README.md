# CBSOT Summer Internship Projects

Repository showcasing end-to-end data science projects developed during the CBSOT internship program.

---

## Project 1: Telco Customer Analytics & Upsell Propensity

Focused on **Churn Prediction**, **Customer Segmentation**, and **Upsell Propensity Analysis**.

### Methodology

#### 1. Exploratory Data Analysis & Data Preparation

* Conducted exploratory analysis to understand dataset shape and composition.
* Performed data cleaning, missing value handling, and preprocessing.

#### 2. Feature Engineering

* Encoded categorical variables.
* Transformed raw customer attributes into model-ready features.

#### 3. Churn Prediction

* Implemented a **Random Forest Classifier**.
* Addressed class imbalance through hyperparameter tuning.
* Achieved:

  * **Recall:** 74% (for predicting most likely churners)
  * **Accuracy:** 78%
  * **ROC-AUC:** 0.857

#### 4. Customer Segmentation

* Applied **K-Means Clustering**.
* Determined the optimal number of clusters using the **WCSS (Elbow Method)**.
* Identified three customer segments as:

  * **Budgeted Loyal Customer**
  * **High Risk New Customer**
  * **Loyal Premium Customer**

---

## Extension: Upsell Propensity Analysis

### Approach

* Built service-specific propensity models to rank upsell opportunities among existing non-holders.
* Evaluated model quality using **ROC-AUC**, **cross-validation stability**, **bootstrap confidence intervals**, and **Logistic Regression benchmarking**.

### Key Findings

* Lower AUC values observed within the **Loyal Premium Customer** segment were attributed to **market saturation effects** rather than model failure.
* Logistic Regression produced performance comparable to Random Forest, indicating that weaker predictive performance stemmed from limited signal in the available features.
* Bootstrap confidence intervals further validated the robustness of these findings.
* High existing adoption rates suggested that Premium non-holders represent a heterogeneous minority-holdout population that is inherently more difficult to characterize.

---

## Top Upsell Opportunities

### Budgeted Loyal Cusomer Segment

* **Online Security** — Strong predictive performance (**AUC ≈ 0.93**)
* **Tech Support** — Stable propensity estimates (**AUC ≈ 0.91**)
* **Online Backup** — High-ranking opportunity (**AUC ≈ 0.89**)
