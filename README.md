## 🧬 Patient Segmentation for Risk Stratification — Unsupervised ML

This project focuses on **segmenting patients into clinically meaningful risk groups** using unsupervised learning.
It simulates a realistic patient cohort with demographics, clinical markers, behavior, and utilization, then applies clustering to uncover patterns that can be used for **risk stratification and population health management**.

---

## 🔍 Project Summary

* Generated a synthetic dataset of **3,000 patients** with:

  * Demographics: age, BMI
  * Clinical markers: HbA1c, cholesterol, comorbidity index
  * Behavior: adherence score, smoking status, exercise minutes
  * Utilization: ER visits, PCP visits, medication count
* Introduced **correlated features** (e.g., higher HbA1c with comorbidities, higher cholesterol with BMI) and **tail-risk patients** (very poorly controlled diabetics, high-utilization “frequent flyers”)
* Standardized features with `StandardScaler` and performed **K-Means clustering**
* Used **silhouette score** to compare different values of *k* and selected an optimal number of clusters
* Built detailed **cluster profiles** summarizing risk, utilization, and behavior per segment
* Applied **PCA** for 2D visualization of patient segments

---

## 🧠 Key Insights

The clustering produced distinct patient segments, for example:

* Older, high-comorbidity patients with elevated HbA1c, high cholesterol, multiple medications, and high ER/PCP utilization
* Moderate-age patients with suboptimal adherence and rising risk markers
* Lower-risk, more adherent patients with better metabolic control and higher exercise levels

These segments reflect **clinically interpretable risk tiers**, useful for:

* Targeted outreach or care management
* Designing intervention strategies for high-risk cohorts
* Understanding utilization drivers across the population

---

## 💼 Real-World Relevance

This type of unsupervised segmentation is a core tool in:

* **Population health analytics**
* **Care management and risk stratification**
* **Resource allocation and program design**
* **Identifying high-cost, high-need patient cohorts**

It enables organizations to move from one-size-fits-all care to **data-driven, segment-specific strategies**.

---

## 🛠 Tech Stack

Python • NumPy • Pandas • scikit-learn • Matplotlib

Methods used:

* Standardization (`StandardScaler`)
* K-Means clustering
* Silhouette analysis
* PCA for dimensionality reduction and visualization

---

## 🚀 Run the Project

```bash
python patient_segmentation_risk_stratification.py
```

This will:

* Generate the synthetic patient dataset
* Run clustering and print cluster profiles
* Output silhouette scores for different k values
* Create a PCA-based 2D scatter plot of patient segments

