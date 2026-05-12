# Diabetes-LLA-Risk-Prediction
This project addresses the "Accuracy Paradox" in clinical datasets where amputation is a sparse event (19% minority class). Our framework shifts focus from global accuracy to Clinical Recall, utilizing a hybrid approach of SMOTE-augmented architectures to identify high-risk patients.

Methodology Implemented :


1. Data Preprocessing & SMOTE: The clinical dataset features a significant class imbalance, with only about 19% of samples representing amputation events. This pipeline uses the Synthetic Minority Over-sampling Technique (SMOTE) restricted strictly to the training folds of a 5-fold stratified cross-validation framework. This prevents data leakage and ensures the algorithms do not succumb to majority-class bias

2. Unsupervised Clustering: Includes K-Means clustering (optimal k=3 via the Elbow Method) to identify three distinct patient phenotypes: chronic systemic vascular compromise, acute metabolic failure, and a lower-acuity stable state

3.  Predictive Modeling: Implements six machine learning classifiers  to predict amputation risk

4.  Model Interpretability (SHAP): Uses SHAP (SHapley Additive exPlanations) values to extract global feature importance, verifying that systemic markers like blood glucose and C-reactive protein (CRP) are the primary drivers of amputation risk rather than localized wound size






