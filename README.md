# DavidZhao_Portfolio
Data science portfolio

# Project 1: Pediatric obesity trajectory prediction: Project Overview
- I built machine learning models to predict the obesity-associated trajectory for young children on 16S rRNA amplicon-based gut microbiota profiles of infants aged three months. The project leads to a robust microbiome-based model that may facilitate precision medicine and to potential biomarkers for prognosis of childhood obesity. 
- The resulting models manifest higher predictive power than existing microbiome-based ML models for childhood obesity prediction. 
- I employed Random Forest, XGBoost, Regularized Logistic Regression and Generalized Linear Mixed Model (GLMM) to the gut microbiota dataset, formulating the ML pipeline dealing with technical issues of repeat measures, imbalanced class, and the batch effect.
- The stratified, repeated, 5-fold Cross-Validataion with SMOTE algorithm help achive the optimal models.   
- GLMM won other four machine learning models, achieving AUC-ROC 0.84 (90% bootstrap CI 0.70, 0.94) on the test set. 
- The optimal GLMM model possessed a sensitivity of 0.9 and specificity of 0.6 under the best threshold. 
- The microbiome-based machine learning models identified five possible gut biomarkers, including Osillospira, Rikenellaceae genus, Blautia, Phascolarctobacterium, and Haemophilus.   

![AUC](https://github.com/davidzhao1015/DavidZhao_Portfolio/blob/main/images/fig3_proj1.png) 

# Project 2: Multiple regression for infant gut health: Project Overview
- Introduction: Health Canada recommends exclusively breastfed, healthy, term infants be supplemented with vitamin D. Vitamin D liquid formulations contain non-medicinal excipients, such as glycerin (glycerol) or propylene glycol (PG). Digested glycerin and PG are fermentable by gut microbiota, producing metabolites likely influencing the host. In this respect, we sought to assess infant fecal samples for the presence of glycerin and PG levels in relation to vitamin D supplementation and their association with gut microbiota and metabolites.   
- Methodology: Fecal samples, information on infant vitamin D supplementation and breastfeeding status were collected at 3 months of age from 575 infants in the Canadian Healthy Infant Longitudinal Development (CHILD) Cohort Study. Fecal metabolites and microbiota were quantified using Nuclear Magnetic Resonance Spectroscopy and 16S rRNA sequencing, respectively. Logistic regression was used to determine the association between vitamin D supplementation and fecal levels of glycerol and PG. Spearman’s rank correlation was used to correlate fecal microbiota and metabolites with glycerol or PG. 
- Results: Seventy-eight percent of exclusively breastfed infants were supplemented with vitamin D drops. Controlling for breastfeeding status, introduction to solids and maternal education, infants supplemented with vitamin D had 1.6 times higher odds of high-level fecal PG (p<0.05), and 41% lower odds of high-level fecal glycerol (p<0.05) compared to the control group. Fecal PG levels were positively correlated with the relative abundance of Lactobacillus spp. (r=0.3, p<0.05), Enterobacteriaceae (r=0.2, p<0.05), Bifidobacterium spp. (r=0.2, p<0.05) but inversely related to Lachnospiraceae (r= -0.3, p<0.05). Accordingly, a higher fecal PG concentration was correlated with higher acetate (r=0.1, p<0.05) but lower butyrate (r= -0.4, p<0.05) and propionate (r= -0.4, p<0.05) levels. 
- Conclusions: Infants supplemented with vitamin D exhibit higher fecal PG levels. The novel link between fecal PG and probiotic microbiota, notably Bifidobacterium, and with microbial acetate, butyrate and propionate may have implications for infant health. 

![multiple linear regression](https://github.com/davidzhao1015/DavidZhao_Portfolio/blob/main/images/tab1.png)
![spearman correlation between gut microbiota and metabolites](https://github.com/davidzhao1015/DavidZhao_Portfolio/blob/main/images/fig1.png)
