<style>
  .heading1{
    color: black;
    font-weight:bold;
    font-size: 200%;
    font-family: Segoe UI;
    line-height: 24px;
  }
  
  .heading2{
    color: black;
    font-weight:bold;
    font-size: 150%;
    font-family: Segoe UI;
    line-height: 24px;
  }
  
  .heading3{
    color: black;
    font-weight:bold;
    font-size: 100%;
    font-family: Segoe UI;
    line-height: 24px;
  }
 
  p {
    line-height: 22px; 
    color:#494949; 
    font-weight:normal;
    font-size: 90%;
    font-famiy:Georgia;
  }
  
</style>
<br/>
<h1 id="identifier" class="heading1">
  Data Science Portfolio 
</h1>

<br/>

<h2 id="identifier" class="heading2">
  🩺Microbiome Epidemiology
</h2>
--- 
<h3 id="identifier" class="heading3">
  Association between vitamin D use and infant gut microbiome, a cohort study
</h3> 

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-warning">Linear Regression</span>
  <span class="tag">Logistic Regression</span>
  <span class="tag">Cohort study</span>
  <span class="tag">Data Reporting</span>
  <span class="tag">R</span>
</div>  

<img src="images/model_infant_vitd.jpg"/>

<p id="identifier" class="p">
Health Canada recommends that exclusively-breastfed newborns should receive sufficient vitamin D every day. In this academic project, my colleagues and I developed a generalized linear model to investigate the relationship between vitamin D use, fecal metabolites, and microbiota, adjusting for covariables. The project used a cohort dataset of 575 infants. Vitamin D use and some prenatal variables were extracted from questionnaires; fecal metabolites and microbiota data were a readout of the NMR spectrum and high-throughput DNA sequencing, respectively. By the Directed Acyclic Graph method, I identified a minimal set of confounder variables for the statistical modeling. This project resulted in a peer-reviewed paper in the journal, Biomolecules (IF = 6.06) in 2023.
</p>
<br/>
[![](https://img.shields.io/badge/PDF-Open_research_poster-B44F99?logo=PDF)](pdf/Poster_vitD_microbiome_david.pdf) 
[![](https://img.shields.io/badge/HTML-View%20artile-yellow)](https://www.mdpi.com/2218-273X/13/2/200)

---
### Multivariate regression of microbiome composition and medical covariables using Human Microbiome Project-IBD dataset 
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-1182C3?logo=GitHub)](html/maaslin2-IBD-microbiome.html) 
#### I build multivariate mixed-effect regression models to investigate the differential abundance of the gut microbiome between non-IBD and IBD patients. As repeated samples exist, I include random-effect variables in the final model. Based on multiple test-corrected p-values, I identify a few significant taxa associated with IBD status. The input data set originates from the IBD database of the Human Microbiome Project. 
<img src="images/image_multi-regression_david.png?raw=false"/>
- **Statistical methods: generalized linear mixed-effect regression; data transformation; multiple test correction**
- **R packages: tidyverse; MaAsLin2**

---
### Models on zero-inflated microbiome (abundance) data
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](html/zero-inflated-models-mcirobiome.html) 
#### Microbiome abundance data often contain excessive zero, which causes rejection of the assumption of traditional statistical models, such as Poisson regression. Fortunately, biostatisticians developed advanced models to address the issue, including zero-inflated Negative Binomial and zero-inflated Poisson, zero-hurdle Negative Binomial, and zero-hurdle Poisson models. I showcase the capability of such models in a case study with the IBD data set of the Human Microbiome Project, following the instruction in the book, Statistical analysis of microbiome with R. Using AIC and likelihood ratio test, I compare performance of candidate models. 
<img src="images/image_zero-inflate_david.png?raw=false"/> 
- **Statistical methods: zero-inflation Poisson/NB; zero-hurdle Poisson/NB**
- **R packages: pscl; lmtest**

---
### Models on over-dispersed microbiome (abundance) data
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](html/overdisp-zeroinflate-model.html) 
#### The microbiome is often over-dispersed other than zero-inflated, which disagrees with the assumption of the Poisson and Quasi-Poisson models. Negative binomial, however, addresses the over-dispersion in microbiome abundance data. I developed an edgeR pipeline to test the diffferential abundance of taxa between non-IBD and IBD patients, following the instruction in the book, Statistical analysis of microbiome with R.
<img src="images/image_overdispersion_david.png?raw=false"/> 
- **Statistical methods: negative binomial regression**
- **R packages: edgeR**

---
### Correlation network analysis of gut microbiota with SparCC python module: considering compositionality inherent in microbiome data
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](https://davidzhao1015.github.io/sparcc-relative-corr2/#1_install_package)
#### Relative abundance data of microbiome is compositional. Classical statistical associations methods, such as Pearson correlation or Spearman rank correlation, are invalid when analyzing compositional data and will lead to spurious correlations. Friedman and Alm developed an alternative method(Friedman and Alm 2012), SparCC to infer the correlation network between taxa from microbiome data, effectively dealing with compositionality. Experiments based on both simulated data and the real data (HMP) proves validity of SparCC.The project aims to demonstrate application of SparCC on a real microbiome dataset, using Python 3 and R language as well as visulaizatoin of the network. 
<img src="images/sparcc_git_profile.jpg"/> 
- **Statistical methods: data transformation; correlation**
- **R packages: SparCC, ggraph, igraph, corrplot**

---
### Proportionality analysis of compositional microbiome data, using a real dataset
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](https://davidzhao1015.github.io/association_analysis_compositional/)
#### One common goal of the microbiome study is to infer dependence relationship between taxa. Relative abundance data of microbiota is compositional data. The classic statistical methods (e.g., Pearson correlation and Spearman rank correlation), however, are invalid for compositional (microbiome) data and leads to spurious correlations.The review article, “Microbiome datasets are compositional: and this is not optional” (Gloor et al. 2017)summarized three valid statistical methods that deal with compositionality in microbiome relative abundance data to achieve reliable inferred correlation, including proportionality and SparCC, Spiec Easi. In this mini-project, I focused on illustrating proportionality analysis on the real microbiome data. Lovell and co-authors (Lovell et al. 2015) proposed the proportionality method for relative correlation, as a valid alternative to absolute correlation. In 2017, Quinn and his colleagues developed the R package, propr to implement the proportionality analysis (Thomas P. Quinn et al. 2017). Based on experiments on simulation datasets, proportionality is a precise indicator of absolute correlation, although sensitivity is limited (Thomas P. Quinn et al. 2017).
<img src="images/propr_profile.jpg"/> 
- **Statistical methods: data transformation; network**
- **R packages: propr, ggraph, igraph, Hmisc** 


## 🤖Machine Learning 
### Classifier of childhood obesity trajectory based on infant fecal microbiome data 
[![](https://img.shields.io/badge/PDF-Open_presentation_slides-C6466B?logo=PDF)](pdf/PPT_predict-child-obesity_davidzhao.pdf)
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](https://github.com/davidzhao1015/infant_microbiota_predict_obesity/blob/main/bmi_traj_pred_infant_microbiota.Rmd) 
#### Knowing obesity risk earlier could help healthcare professionals manage children's weight more effectively. According to the literature review, microbiome composition and functions plays a vital role in overweight development in children. My team proposed including fecal microbiome data in the classifiers to devise a statistical prediction tool to predict future obesity risk. I trained Random Forest, XGBoost, GLMM, and regularized logistic classifiers based on fecal microbiome data of nearly 2000 infants. Based on the ROC-AUC of the validation procedure, I found GLMM-classifier the best with an AUC of 0.83, specificity of 73%, and sensitivity of 85% at the best threshold. In addition, I identified five microbial biomarkers at the genus level with good predictive ability. 
<img src="images/fig3_proj1.png?raw=false"/>
- **Statistical methods: Random Forest; XGBoost; Generalzied linear mixed model; regLog; cross-validation**
- **R packages: caret**

---

## 🧬Genomic Bioinformatics
### Comparative genomics of gut and sourdough lactobacilli 
[![](https://img.shields.io/badge/PDF-Open_presentation_slides-C6466B?logo=PDF)](pdf/PPT_phd_david.pdf)  
#### This is part of my Ph.D. research project. My colleagues and I worked on genomic adaption for strains from rodent guts to back-slopping sourdoughs. Using comparative genomics techniques, we identified particular genes under the "positive selection", including carbohydrate metabolism genes. In this sense, I developed the in-house bioinformatic pipeline to locate subtle genetic differences among strains commensal to rodents and sourdoughs. The project's discovery may help better explain genetic adaption for lactobacilli between different ecological niches and support start culture and probiotics development. 
<img src="images/image_comparative-genomics.png?raw=false"/>
- **Software: standalone BLAST toolkit; MEGA 5; MAUVE; KEGG server**


