# Diabetes-LLA-Risk-Prediction
This project addresses the "Accuracy Paradox" in clinical datasets where amputation is a sparse event (19% minority class). Our framework shifts focus from global accuracy to Clinical Recall, utilizing a hybrid approach of SMOTE-augmented architectures to identify high-risk patients.

Methodology Implemented :


1. Data Preprocessing & SMOTE: The clinical dataset features a significant class imbalance, with only about 19% of samples representing amputation events. This pipeline uses the Synthetic Minority Over-sampling Technique (SMOTE) restricted strictly to the training folds of a 5-fold stratified cross-validation framework. This prevents data leakage and ensures the algorithms do not succumb to majority-class bias

2. Unsupervised Clustering: Includes K-Means clustering (optimal k=3 via the Elbow Method) to identify three distinct patient phenotypes: chronic systemic vascular compromise, acute metabolic failure, and a lower-acuity stable state

3.  Predictive Modeling: Implements six machine learning classifiers  to predict amputation risk

4.  Model Interpretability (SHAP): Uses SHAP (SHapley Additive exPlanations) values to extract global feature importance, verifying that systemic markers like blood glucose and C-reactive protein (CRP) are the primary drivers of amputation risk rather than localized wound size


### Citation

If you find this repository or code useful in your research, please consider citing the following paper: 


Menon, G. R., Jose, S. A., Jose, S., Thomas, J. K., & Jirawattanapanit, A. (2026). Predicting lower limb amputation risk based on clinical factors and wound characteristics using machine learning. Physica Scripta, 101, Article 105004

Data Source Acknowledgment: The clinical dataset (shq_data.csv) used in this repository is publicly available 
