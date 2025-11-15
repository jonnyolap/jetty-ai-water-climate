# Project 1: Water Quality AI

## Project Status:

Status: Analysis Complete. Model requires further Retraining (Phase 4) to address the unacceptably high False Negative Rate for production deployment.

Access the analysis and model results here: [01_Water_Quality_Analysis.ipynb](notebooks/1.0-Water-Quality-Data-Acquisition.ipynb)
---

The classification model shows a strong ability to detect Unsafe Water (88.6% True Negative Rate). However, it exhibits a critical safety flaw: a 63.9% False Negative Rate in the "Safe" class. This means the model incorrectly predicts over half of contaminated samples as safe, confirming the need for a major retraining effort before deployment.

## Summary
This project established a baseline Logistic Regression model with SMOTE to classify water quality.

The classification model shows a strong ability to detect Unsafe Water with an 88.6% True Negative Rate. However, it exhibits a critical safety flaw: a 63.9% False Negative Rate in the "Safe" class.

This means the model incorrectly predicts over half (156 samples) of the contaminated water as safe, confirming the need for a major retraining effort before deployment. The key finding is the need for further model tuning to reduce these 156 False Negatives (missed contamination risks).

## Deployment Strategy:

Next Phase: The final model will be intensively retrained using advanced hyperparameter tuning and feature engineering to prioritize Recall (reducing False Negatives) before deployment on the dedicated DigitalOcean MLOps Droplet.
