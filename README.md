# DavidZhao_Portfolio
Data science portfolio

# Project 1: Pediatric obesity trajectory prediction: Project Overview
- I built machine learning models to predict the obesity-associated trajectory for young children on 16S rRNA amplicon-based gut microbiota profiles of infants aged three months. 
- The resulting models manifest higher predictive power when compared to existing microbiome-based ML models for childhood obesity prediction. The project provides a robust microbiome-based model to facilitate precision interventions for clinicians and identify a group of biomarkers for the diagnosis and prognosis of childhood obesity. 
- I employed Random Forest, XGBoost, Regularized Logistic Regression and Generalized Linear Mixed Model (GLMM) to the gut microbiota dataset, formulating the ML pipeline dealing with technical issues of repeat measures, imbalanced class, and the batch effect.
- The stratified, repeated, 5-fold Cross-Validataion with SMOTE algorithm help achive the optimal models.   
- GLMM won other four machine learning models, achieving AUC-ROC 0.84 (90% bootstrap CI 0.70, 0.94) on the test set. 
- The optimal GLMM model possessed a sensitivity of 0.9 and specificity of 0.6 under the best threshold. 
- The microbiome-based machine learning models identified five microbial biomarkers at the genus level, including Osillospira, Rikenellaceae genus, Blautia, Phascolarctobacterium, and Haemophilus.   

# Project 2: Multiple logistic regression for infant gut health
