# Customer Churn Prediction for E-Commerce

A predictive modeling system that identifies customers at risk of churning, deployed as a real-time scoring API and paired with a business dashboard — turning model output into targeted retention action.

---

## Overview

Retaining an existing customer is far cheaper than acquiring a new one. This project predicts which e-commerce customers are likely to churn, identifies *why*, and feeds those predictions into retention campaigns. The model was deployed for real-time scoring and connected to a Power BI dashboard so business teams could act on customer risk and lifetime-value impact directly.

## Approach

**Exploratory data analysis**
- Investigated behavioral and transactional patterns to find the strongest churn signals.
- Key drivers identified: **inactivity periods** and **low engagement**.

**Feature engineering**
- Engineered **RFM features** (Recency, Frequency, Monetary value) — a classic, high-signal framing for customer behavior — which boosted model accuracy by ~15% through better feature selection.

**Modeling**
- Trained and compared **XGBoost** and **Random Forest** classifiers.
- Best model reached **~92% precision** on churn prediction.

**Deployment & business integration**
- Served the model through a **Flask API** for real-time customer risk scoring.
- Built a **Power BI dashboard** tracking churn probability and customer-lifetime-value (CLTV) impact.
- Insights drove **~12% higher retention** via targeted email campaigns.

## Results

| Metric | Value |
|---|---|
| Churn precision | ~92% |
| Accuracy lift from RFM features | +15% |
| Retention improvement | +12% |

## Tech Stack

`Python` · `XGBoost` · `Random Forest` · `scikit-learn` · `Flask` · `Power BI` · `pandas`

## Architecture

```
Raw customer data → RFM feature engineering → XGBoost / Random Forest
        → Flask API (real-time scoring) → Power BI dashboard (churn + CLTV)
        → Targeted retention campaigns
```

## Future Work

- Add probability calibration so risk scores map to true churn likelihood.
- Incorporate time-series / sequence features to capture behavior trends.
- A/B test retention interventions to measure causal lift.

> **Note:** This project was developed in a cloud environment; source files are being reconstructed. The repository documents the methodology, architecture, and results.

---

*Built by [Akhil Karumanchi](https://github.com/Akhilkarumanchi05) · [LinkedIn](https://www.linkedin.com/in/akhil-karumanchi-56440922a/)*
