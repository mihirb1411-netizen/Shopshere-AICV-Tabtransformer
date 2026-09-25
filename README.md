# 🛍️ ShopSphere — AICV TabTransformer
## 🚀 Live Demo

**Try the interactive ShopSphere AICV application:**

[![Open Live Demo](https://img.shields.io/badge/🚀_Open_Live_Demo-Hugging_Face-orange?style=for-the-badge)](https://huggingface.co/spaces/Mihirrish/ShopSphere-AICV-TabTransformer-v2-Demo)
### Algorithm-Induced Customer Churn Volatility Detection using TabTransformer

[![Hugging Face Demo](https://img.shields.io/badge/🤗%20Live%20Demo-Hugging%20Face-yellow)](https://huggingface.co/spaces/Mihirrish/ShopSphere-AICV-Demo)
[![Model Format](https://img.shields.io/badge/Model-ONNX-blue)](https://onnx.ai/)
[![Frontend](https://img.shields.io/badge/Frontend-HTML%20%7C%20CSS-orange)](#technology-stack)
[![Status](https://img.shields.io/badge/Status-Completed-success)](#project-status)

---

## 📌 Project Overview

**ShopSphere — AICV TabTransformer** is an AI-driven customer churn analysis system designed to identify and quantify sudden changes in customer churn caused by external platform-level algorithmic changes.

The project introduces the concept of **Algorithm-Induced Customer Churn Volatility (AICV)**, which measures the relative increase in customer churn following a significant external platform algorithm update compared with the historical baseline churn rate.

The project combines:

- Customer behavior analytics
- Churn analysis
- Algorithmic impact measurement
- Tabular deep learning
- TabTransformer architecture
- ONNX model deployment
- Interactive web-based visualization

The objective is to provide a structured way of identifying whether an unusual increase in customer churn may be associated with a platform algorithmic change rather than normal customer behavior.

---

# 🎯 Problem Statement

Traditional customer churn models generally focus on customer-level factors such as:

- Purchase frequency
- Spending behavior
- Customer tenure
- Engagement
- Product interactions
- Demographic characteristics

However, customer churn can also be affected by **external platform-level changes**, such as changes to recommendation algorithms, product visibility, ranking systems, pricing access, or digital exposure.

A sudden algorithmic change can alter how products and customers interact with a platform, potentially resulting in an abnormal increase in customer cancellations.

The project therefore addresses the following problem:

> **How can organizations identify and quantify unusual customer churn volatility associated with an external platform algorithm update?**

---

# 💡 Proposed Solution

ShopSphere introduces **AICV (Algorithm-Induced Customer Churn Volatility)** as a metric for comparing post-algorithm-update churn against the historical churn baseline.

### AICV Formula

\[
\text{AICV} =
\frac{\text{Post-Algorithm-Update Churn Rate}}
{\text{Historical Baseline Churn Rate}}
\]

### Interpretation

| AICV Value | Interpretation |
|---|---|
| AICV ≈ 1 | Churn remains close to historical levels |
| AICV > 1 | Churn is higher than the historical baseline |
| AICV significantly > 1 | Potentially abnormal churn volatility following the update |
| AICV < 1 | Churn is lower than the historical baseline |

AICV is intended as an **analytical indicator**, not as standalone proof that an algorithm update caused customer churn.

---

# 🧠 Why TabTransformer?

The project uses a **TabTransformer** architecture for analyzing structured/tabular customer data.

Traditional machine learning models can perform well on structured datasets, but customer behavior often contains complex relationships between categorical and numerical variables.

TabTransformer uses attention mechanisms to learn contextual relationships between categorical features.

This makes it suitable for datasets containing combinations of:

- Customer attributes
- Transaction behavior
- Product interactions
- Engagement indicators
- Platform exposure
- Churn-related variables

---

# 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │   Customer Dataset   │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Data Preparation &    │
                    │ Feature Engineering   │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   TabTransformer     │
                    │   Model Training     │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Model Export to ONNX │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Web-Based Prediction │
                    │      Interface       │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ AICV / Churn Output  │
                    └──────────────────────┘
