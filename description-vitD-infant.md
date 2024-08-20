---
layout: page
title: Project Description for Vitamin D and Infant Gut Health 
permalink: /project_description_vitaminD_infant_gut/
---

# project Description: Vitamin D and Infant Gut Health, A Regression Analysis

## Introduction
    
Health Canada recommends that all exclusively breastfed, healthy, full-term infants receive 400 IU of vitamin D daily until they obtain sufficient amounts from other sources. Infant vitamin D liquid formulations often include non-medicinal excipients, such as glycerin and 1,2-propanediol (1,2-PD), which are inactive substances used as carriers for the active drug. However, the effects of these excipients on the infant gut environment have not been thoroughly studied.
    
Previous research has indicated that Veillonellaceae, a type of gut bacteria, decreases in breastfed infants who are supplemented with vitamin D, mirroring trends seen in adults.
    
In this analysis, I investigated the impact of vitamin D drops on key gut metabolites and microbes in three-month-old infants. Using multiple regression modeling, the study integrates data from metabolomics, microbiome profiling, and medical records from the CHILD (Canadian Healthy Infant Longitudinal Development) Cohort Study, a large prospective birth cohort in Canada. This approach aims to shed light on how vitamin D supplementation and its non-medicinal components influence the infant gut microbiota.
    
## Data
    
This study analyzed data from 575 infants in the CHILD Cohort Study, accessed on September 1, 2021 ([www.childstudy.ca](http://www.childstudy.ca/)).
    
Fecal Metabolites: Quantified as µmol/g of feces using NMR spectroscopy.
    
Fecal Microbiota: Collected at 3.7 months (SD = 1.2), analyzed for microbial taxa relative abundance via 16S rRNA gene sequencing on Illumina.
    
Covariates: Included delivery mode, feeding practices, antibiotic use, maternal BMI, vitamin use, socioeconomic status, and infant age at stool collection. Data were collected via birth records and standardized questionnaires.
    
## Analysis

- **Missing Data**: Samples with missing values were excluded from the analysis.
- **Data Transformation and Normalization**: For logistic regression, fecal metabolite concentrations were converted into binary variables (high vs. low levels). For linear regression, concentrations (in µmol/g) were log-transformed to meet model assumptions.
- **Directed Acyclic Graph (DAG)**: A DAG was used to identify a minimal set of covariates based on a literature review. The 15% change-in-estimate criterion was applied to finalize the covariates for adjustment.
- **Logistic Regression**: Logistic models were used to assess the impact of vitamin D drops on fecal glycerol and 1,2-PD, with metabolite levels as independent variables and vitamin D drops as the dependent variable. Covariates included feeding mode, introduction of solids at 3 months, maternal education, and age of stool collection.
- **Linear Regression**: Linear models were constructed to further explore the impact of vitamin D on the two target fecal metabolites, using log-transformed concentrations as independent variables, with categorical and numerical variables as dependent variables.
- **Spearman Correlation**: Spearman correlation analysis was performed to examine associations between fecal glycerol or 1,2-PD and gut microbes as well as short-chain fatty acids.

## Results

Vitamin D supplementation was linked to a higher likelihood of elevated 1,2-PD levels (adjusted OR 1.65, 95% CI: 1.06–2.53) and a lower likelihood of elevated fecal glycerol levels (adjusted OR: 0.62, 95% CI: 0.42–0.90) after accounting for breastfeeding and other factors. These results were consistent in linear regression models, showing that vitamin D supplementation was positively associated with 1,2-PD and negatively associated with glycerol (adjusted β: 0.37, 95% CI 0.03–0.71; adjusted β: −0.23, 95% CI −0.44–−0.03). 

Additionally, 1,2-PD and glycerol levels were negatively correlated, and 1,2-PD was positively correlated with Bifidobacteriaceae, Lactobacillaceae, Enterobacteriaceae, and acetate levels.

## Contribution

Our research shows that administering vitamin D supplements to infants may have distinct and independent effects on the metabolites produced by the infant gut microbiota.

## Acknowledgments

Professor Dr. Anita Kozryskyj supervised the study, with statistical analysis and R programming support provided by colleagues in the SyMBIOTA group.


