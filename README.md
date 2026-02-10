# ⚙️ Smart Industrial Predictive Maintenance

> A machine learning classification system that predicts **equipment failures** in industrial machinery using sensor data — covering the full journey from exploratory data analysis to multi-model evaluation and comparison.

---

## 📋 Problem Statement

Unplanned equipment downtime is one of the **costliest challenges** in industrial operations. Traditional maintenance strategies — either reactive (fix after failure) or scheduled (fix on a calendar) — are both inefficient:

- **Reactive maintenance** leads to expensive emergency repairs and production losses
- **Scheduled maintenance** often replaces parts that still have useful life remaining

**Predictive maintenance** solves this by using sensor data and machine learning to forecast failures *before* they happen, enabling **just-in-time intervention**.

This project builds classification models to predict whether a machine will fail, using operational parameters like temperature, torque, rotational speed, and tool wear.

---

## 📊 Dataset Overview

The dataset contains **10,000 records** of industrial machinery sensor readings with the following features:

| Feature | Description | Unit |
|---|---|---|
| `Type` | Product quality variant (L / M / H) | Category |
| `Air temperature [K]` | Ambient air temperature | Kelvin |
| `Process temperature [K]` | Internal process temperature | Kelvin |
| `Rotational speed [rpm]` | Machine rotational speed | RPM |
| `Torque [Nm]` | Applied torque | Newton-meters |
| `Tool wear [min]` | Cumulative tool usage time | Minutes |
| `Target` | Binary failure flag (0 = No Failure, 1 = Failure) | — |
| `Failure Type` | Type of failure (if any) | Category |

### Failure Types Analyzed
- **Heat Dissipation Failure** — Temperature differential exceeds thresholds
- **Power Failure** — Torque × rotational speed falls below operational limits
- **Overstrain Failure** — Excessive tool wear combined with high torque
- **Tool Wear Failure** — Tool replacement threshold exceeded
- **Random Failure** — Probabilistic failures independent of parameters

---

## 🏗️ Project Workflow

```
┌──────────────┐    ┌──────────────┐    ┌──────────────────┐
│  Load Data   │───►│     EDA      │───►│  Data            │
│  (CSV)       │    │  (Visualize  │    │  Preprocessing   │
│              │    │   & Analyze) │    │  (Clean, Encode, │
│              │    │              │    │   Scale)          │
└──────────────┘    └──────────────┘    └────────┬─────────┘
                                                 │
┌──────────────┐    ┌──────────────┐    ┌────────▼─────────┐
│  Compare     │◄───│  Evaluate    │◄───│  Model Training  │
│  Results &   │    │  (Accuracy,  │    │  (Multiple       │
│  Select Best │    │   Precision, │    │   Algorithms)    │
│              │    │   Recall, F1)│    │                  │
└──────────────┘    └──────────────┘    └──────────────────┘
```

---

## 🧰 Tech Stack

| Category | Technologies |
|---|---|
| **Language** | Python |
| **Data Analysis** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Machine Learning** | Scikit-learn (Logistic Regression, Decision Trees, Random Forest, Gradient Boosting, etc.) |
| **Progress Tracking** | tqdm |
| **Environment** | Google Colab / Jupyter Notebook |

---

## 📂 Project Structure

```
Smart-Industrial-Predictive-Maintenance/
├── Machine_Predictive_Maintenance_Classification.ipynb   # Full analysis notebook
├── predictive_maintenance.csv                            # Dataset (10,000 records)
├── requirements.txt                                      # Dependencies
└── README.md
```

---

## ✨ Key Features

- **Comprehensive EDA** — Distribution analysis, correlation heatmaps, class balance visualization, and outlier detection across all sensor features.
- **Feature Engineering** — Creating derived features and encoding categorical variables (product quality types L/M/H).
- **Multi-Model Comparison** — Training and evaluating multiple classification algorithms side-by-side.
- **Failure Type Analysis** — Not just binary prediction but understanding *which type* of failure is most likely.
- **Performance Metrics** — Evaluation using accuracy, precision, recall, F1-score, and ROC-AUC — critical for imbalanced industrial datasets where false negatives (missed failures) are costly.

---

## 🧠 My Learning Journey

This was my deep-dive into the **data science workflow** — understanding that building a model is only a small part of the actual work.

| Area | What I Learned |
|---|---|
| **Exploratory Data Analysis** | The importance of *understanding your data before modeling* — distributions, correlations, and outliers tell you more than any model. I spent significant time visualizing each feature's relationship with failures. |
| **Handling Imbalanced Data** | Industrial failure datasets are inherently imbalanced (failures are rare events). I learned why accuracy alone is misleading and why precision/recall trade-offs matter for predictive maintenance. |
| **Feature Engineering** | Deriving new features from domain knowledge — e.g., temperature differentials, power calculations (torque × RPM) — and understanding which features have the strongest predictive signal. |
| **Model Selection** | Comparing multiple algorithms taught me that there's no "best" model — the right choice depends on the data characteristics and business requirements (cost of false positives vs. false negatives). |
| **Domain Connection** | My mechanical engineering background helped me understand *why* certain features predict failures — e.g., the physics behind heat dissipation failure modes. |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Jupyter Notebook or Google Colab

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/Smart-Industrial-Predictive-Maintenance.git
cd Smart-Industrial-Predictive-Maintenance

# Install dependencies
pip install -r requirements.txt
```

### Run the Analysis

```bash
jupyter notebook Machine_Predictive_Maintenance_Classification.ipynb
```

Or upload the notebook directly to [Google Colab](https://colab.research.google.com/).

---

## 📈 Sample Results

The notebook evaluates models on the following metrics:

| Metric | Why It Matters for Predictive Maintenance |
|---|---|
| **Precision** | Avoid unnecessary (costly) maintenance shutdowns |
| **Recall** | Catch as many real failures as possible before they happen |
| **F1-Score** | Balance between precision and recall |
| **ROC-AUC** | Overall model discriminatory power |

---

## 📄 License

This project is open-source. Feel free to use, modify, and distribute.
