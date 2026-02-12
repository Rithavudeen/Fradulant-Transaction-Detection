# 🔍 Fraudulent Transaction Detection Using Anomaly Detection

A machine learning project focused on identifying **fraudulent financial transactions** using **unsupervised anomaly‑detection techniques** and behavioral transaction data to support **real‑time fraud monitoring and investigation workflows**.

---

## 📌 Project Overview

This project implements a complete **end‑to‑end anomaly detection pipeline** that includes:

* Ingestion of **transactional and behavioral data**
* Exploratory data analysis to distinguish **normal vs anomalous activity patterns**
* Feature engineering to capture **irregular spending behavior and deviations**
* Application of **unsupervised anomaly‑detection models**
* Evaluation of detection effectiveness and fraud‑risk insights

The primary objective is to **detect likely fraud without heavy reliance on labeled data**, enabling scalable monitoring in real‑world financial systems.

---

## 🧰 Tech Stack

**Language:** Python
**Libraries:** pandas, numpy, matplotlib, seaborn, scikit‑learn
**Environment:** Jupyter Notebook / Google Colab
**Techniques:** Isolation Forest, Local Outlier Factor, One‑Class SVM, Autoencoders (anomaly detection)

---

## 🔄 Workflow Summary

### 1️⃣ Data Collection

Transaction dataset includes attributes such as:

* Transaction amount and timestamp
* Merchant category and geographical location
* Account history and behavioral indicators
* Other contextual transaction signals

A key challenge addressed is **severe class imbalance**, where fraud cases are rare compared to normal transactions.

### 2️⃣ Exploratory Data Analysis (EDA)

Analytical exploration performed to understand anomaly behavior:

* Distribution of **transaction values, frequencies, and merchant categories**
* Visualization of **unusual spending patterns** (large amounts, rare locations, abnormal times)
* Correlation checks, missing‑value handling, and outlier inspection
* Examination of **data imbalance and anomaly prevalence**

### 3️⃣ Feature Engineering

Constructed behavioral and statistical features including:

* Transaction amount relative to **user’s historical average**
* **Transaction frequency** per account or time window
* Deviation from **normal spending behavior**
* Time‑of‑day and day‑of‑week indicators
* Encoding of categorical variables (merchant type, region)
* Scaling and optional **dimensionality reduction** for anomaly detection

### 4️⃣ Modeling (Unsupervised Anomaly Detection)

Applied anomaly‑detection algorithms that treat fraud as **rare deviations**:

* **Isolation Forest**
* **Local Outlier Factor (LOF)**
* **One‑Class SVM**
* **Autoencoder‑based anomaly detection**

Key steps include:

* Computing **anomaly scores** for transactions
* Selecting **thresholds** (e.g., top 1% highest scores flagged)
* Optionally combining models via **ensemble strategies** to improve recall

### 5️⃣ Evaluation & Insights

Model effectiveness assessed using:

* Recall of known fraud cases (when labels available)
* Precision to control **false alerts**
* ROC‑AUC where partial labels exist

Insights derived include:

* Behavioral patterns that frequently trigger fraud alerts
* High‑risk merchants, regions, or abnormal spending behaviors
* Prioritized **investigation queues** instead of rigid classification

---

## 📁 Project Structure

```
Fraudulent-Transaction-Detection/
│── data/
│── notebooks/
│── src/
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Strong anomaly indicators include **large deviations from baseline spending** and **transactions outside normal time/location windows**
* Unsupervised models effectively flag **suspicious transactions for investigation**
* Carefully tuned thresholds balance **fraud detection vs alert volume**
* Behavioral feature engineering significantly improves detection compared to raw transaction data
* The system supports **fraud‑analysis teams with prioritized alerts** rather than binary labels

---

## 🚀 Future Improvements

* Introduce **supervised or semi‑supervised hybrid models** when labeled fraud data becomes available
* Implement **real‑time streaming architecture** for live fraud scoring
* Add **model explainability** (e.g., SHAP) for investigator transparency
* Periodically **retrain and recalibrate** to handle evolving fraud patterns and model drift
* Expand feature space with **device fingerprinting, geolocation drift, and merchant‑network analytics**

---

## 🎯 Learning Outcomes

* Practical experience with **unsupervised anomaly detection in finance**
* Strong understanding of **behavioral feature engineering and imbalance challenges**
* Exposure to **real‑world fraud monitoring system design**

---

## 🤝 Contribution

Contributions, suggestions, and improvements are welcome. Feel free to fork the repository and submit a pull request.

---

## ⭐ Support

If you found this project useful, consider **starring the repository** and sharing feedback.
