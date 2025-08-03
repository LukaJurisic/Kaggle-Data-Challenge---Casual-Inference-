# 🧪 Causal Inference — Criteo Uplift Modeling

An applied machine learning project using real-world Criteo data to measure the incremental effect of ad exposure. This project highlights **uplift modeling**, a powerful technique for decision-making when traditional classification isn't enough.

> 🎯 Built for interpretable causal analysis — not just prediction.

---

## 🧾 Dataset

- **Source**: [Criteo Uplift Modeling Dataset (Kaggle)](https://www.kaggle.com/datasets/criteo-uplift/uplift-modelling)
- **Size**: 140K+ samples
- **Context**: Ad exposure logs with binary treatment/control, conversions, and anonymized features

---

## 💡 Objective

Instead of predicting who will convert, the goal is to identify **who will convert _because_ they saw an ad**. This is modeled via **uplift** — the incremental effect of treatment vs control.

---

## 🧪 Techniques Used

| Step                           | Tools / Methods                                 |
|--------------------------------|--------------------------------------------------|
| Data Cleaning                  | Pandas, NumPy                                    |
| Balanced Sampling              | Stratified subsampling by treatment             |
| Uplift Modeling                | 2-model approach with LightGBM                  |
| Uplift Curve Analysis          | Qini & Uplift Curves                            |
| Feature Attribution            | SHAP (treatment & control models separately)    |
| Interpretation                 | Net uplift gain, top features, visual ranking   |

---

## 📊 Key Visuals

| Insight Area                  | Output File Name             |
|-------------------------------|------------------------------|
| Uplift Curve (sorted ranking) | `uplift_curve.png`          |
| Qini Curve                    | `qini_curve.png`            |
| SHAP: Treatment Model         | `shap_treatment.png`        |
| SHAP: Control Model           | `shap_control.png`          |
| Feature Attribution Diff      | `shap_diff_barplot.png`     |
| Delta SHAP vs Uplift Score    | `delta_vs_uplift_scatter.png`|

All plots exported in `.png` format and designed for clean, web-optimized display.

---

## 💬 Key Findings

- Top uplift-driving features differ between treatment and control groups — a key insight missed by vanilla classifiers.
- Visualizing the **delta SHAP** between models highlighted features that were positively leveraged _only_ in the presence of an ad.
- The uplift model improved targeting efficiency by 20% in the top decile.

---

## 🖥️ Portfolio Integration

This project is integrated into my interactive personal site powered by React, Tailwind, and Firebase.

🔗 [Explore the Web Showcase](https://yourwebsite.com/criteo-causal-inference)

---

## 🚀 Getting Started

1. Clone the repo  
   ```bash
   git clone https://github.com/LukaJurisic/Criteo-Causal-Inference.git
   cd Criteo-Causal-Inference
