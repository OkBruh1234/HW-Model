# 🌡️ Heat Index Forecasting & Heatwave Detection Model (HI-LSTM)

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-LSTM-green)
![Status](https://img.shields.io/badge/Project%20Status-Preview%20%2F%20WIP-yellow)

---

## 📌 Project Overview

This repository contains a **Heat Index (HI) forecasting and heatwave detection model** developed as part of my **ongoing research and internship work at NIT Delhi**.

The objective of this project is to:
- **Forecast the next 7 days of Heat Index (HI)** using historical meteorological data.
- **Detect heatwave events** (HI ≥ 40 °C) in advance using a hybrid deep learning approach.

⚠️ **Important Note:**  
This project is currently in a **preview / development stage**.  
The implementation works at a **basic functional level**, and **final optimizations, refinements, and validations are still in progress**.

---

## 🧠 What This Project Does (Simple Explanation)

1. Takes **past 30 days of weather-related features**
2. Uses a **deep learning model** to:
   - Predict **Heat Index values for the next 7 days**
   - Predict whether a **heatwave will occur** in that 7-day window
3. Applies **hybrid decision logic** to improve heatwave recall
4. Evaluates performance using **regression and classification metrics**

This approach is designed to **prioritize early heatwave detection**, even at the cost of some false positives — which is critical for real-world heat risk monitoring.

---

## 🏗️ Model Architecture (High Level)

- **Conv1D layers** → capture short-term temporal patterns  
- **Bidirectional LSTM layers** → learn long-term dependencies  
- **Attention mechanism** → focus on critical time steps  
- **Multi-task learning**:
  - 🔹 Regression head → 7-day HI forecast
  - 🔹 Classification head → heatwave detection (binary)

Additional techniques used:
- Data leakage–free scaling
- Weighted regression loss (higher weight for heatwave days)
- Focal loss for imbalanced classification
- Threshold tuning & hybrid voting logic


## 🧪 Current Status

✔️ Data preprocessing and sequence generation
✔️ Leakage-free train/validation/test split
✔️ Multi-task LSTM model implemented
✔️ Basic evaluation and heatwave detection logic
⚠️ Threshold tuning and calibration ongoing
⚠️ Model stability and deployment readiness pending

This codebase should be considered a research-oriented prototype, not a production-ready system.

🚫 Usage & License
⚠️ Confidential Project – Please Read Carefully

This repository is shared for viewing and demonstration purposes only.

© 2025 Arnav Shrivastav. All rights reserved.


❌ Reuse, redistribution, or modification of this code is not permitted

❌ Commercial or academic reuse without permission is strictly prohibited

✅ The repository is intended to showcase project work and methodology only

If you are interested in collaboration or authorized usage, please contact me at jimmyroxx18@gmail.com. 

## 🙏 Acknowledgements

This work is part of my ongoing internship and research activities at NIT Delhi.
I acknowledge the academic guidance and support provided during the course of this project.

## 📬 Contact

Author: Arnav Shrivastav
📧 For inquiries specifications: feel free to reach me out through my LinkedIn: https://www.linkedin.com/in/aarnav-shrivastav-a43001308/ or email: jimmyroxx18@gmail.com

# ⚠️ This repository reflects an active work in progress.
Improvements, restructuring, and final research conclusions are yet to be integrated.

## 📂 Repository Structure

```text
HW-Model/
│
├── HI_Model_Train_best_run.ipynb
│   └─ Main notebook for model training, evaluation, and analysis
│
├── HI&SM_correlation_best_run.ipynb
│   └─ Exploratory analysis on Heat Index relationships
│
└── README.md
