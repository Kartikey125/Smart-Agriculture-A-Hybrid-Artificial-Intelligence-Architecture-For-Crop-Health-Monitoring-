# Smart Agriculture: A Hybrid AI Architecture for Crop Health Monitoring

**Institution:** Jaypee University of Information Technology (JUIT)  
**Course:** Major Project - I (AY 2026-27)  

## Project Overview
Modern precision agriculture relies on high-resolution multispectral remote sensing and automated IoT environmental sensors to track crop health. However, processing this high-dimensional telemetry directly often leads to severe overfitting and model degradation due to overlapping spectral indices and covarying microclimate metrics. 

This project introduces a unified, multi-phase machine learning architecture evaluated on a large-scale agricultural dataset (~212k records). It pairs mathematically rigorous multicollinearity purging with an advanced hybrid modeling pipeline—integrating gradient-boosted trees and deep tabular transformers within a stacking ensemble.

## System Architecture (5-Phase Pipeline)

1. **Data Ingestion & Cohort Preprocessing:** Synchronizing multimodal sensor streams and discretizing target variables into distinct crop stress tiers (Low, Moderate, Severe).
2. **Statistical Redundancy Purge:** Implementing an automated filtering pipeline using a Spearman Rank Correlation filter (|ρ| > 0.85) followed by iterative Variance Inflation Factor (VIF) pruning (VIF ≤ 5.0) to purge collinear features.
3. **Multi-Metric Feature Selection:** Evaluating feature subsets using ANOVA F-test, Mutual Information, and L1 Regularization.
4. **Model Tournament & Stacking Ensemble:** Benchmarking diverse classifiers (XGBoost, CatBoost, Random Forest, FT-Transformer) and combining their Out-of-Fold (OOF) predictions using a regularized Logistic Regression meta-learner.
5. **Explainability & Deployment:** Utilizing SHAP (TreeExplainer/DeepExplainer) to attribute environmental drivers of crop stress, deployed via an interactive Streamlit dashboard for real-time agronomic alerts.

## Current Project Status
**Phase:** Initial Evaluation & Architectural Design

This repository currently houses the foundational architectural flowcharts, methodology blueprints, and literature synthesis documentation. Implementation of the automated data pipeline and FT-Transformer models will commence in the subsequent development phases.
