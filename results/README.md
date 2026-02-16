# 📊 Experimental Results & Clinical Validation

This directory contains the visual and quantitative evidence of the **MetaGuard-3S** performance.

## 📈 Performance Evolution
We tracked the model's improvement across different development phases:

## 📊 Clinical Validation Results

We evaluated the model's performance in two distinct phases to measure the impact of the Meta-Stacking architecture:

### 🔹 Phase 1: Hybrid Base Ensemble (XGB + RF + StatMap)
* **Status:** High sensitivity but limited by high False Negatives in borderline cases.
* **Detection Performance:** Successfully identified **907** metastasis cases.
* **Artifact:** `results/plots/confusion_matrix_hybrid.png`

### 🔹 Phase 2: Final Stacking Layer (MetaGuard-3S / LR Meta-Learner)
* **Status:** Fully optimized for clinical reliability using Logistic Regression to calibrate probabilities.
* **Detection Performance:** Successfully identified **988** metastasis cases.
* **Key Improvement:** Caught an additional **81 patients** through the stacking process alone, before the Safety Net review.
* **Artifact:** `results/plots/confusion_matrix_final.png`

## 🛡️ Safety Net Impact
The most critical result of this study is the **Uncertainty-Aware triage**.
* **Rescued Patients:** **186** individuals who were initially missed by the AI but caught in the 0.416 - 0.616 probability zone.
* **Efficiency:** Prevented **1,756** unnecessary diagnostic procedures.

---
*Note: All plots were generated using Seaborn and Matplotlib within the main pipeline notebook.*
