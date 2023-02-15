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
    font-size: 110%;
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
<br/>
<h3 id="identifier" class="heading3">
Table of Contents
</h3> 
1. [Microbiome Epidemiology](#topic1)<br>
  1.1 [Impact of vitamin D supplements on infant gut microbiome](#subtopic1)<br>
  1.2 [Gut microbiota variations between IBD versus healthy adults](#subtopic2)<br>
  1.3 [Benchmarking algorithms on zero-excessive metagenome data](#subtopic3)<br>
  1.4 [Differential analysis of microbiota data with over-dispersion using edgeR package](#subtopic4)<br>
  1.5 [Correlation network development for gut microbial taxa using SparCC](#subtopic5)<br>
  1.6 [Proportionality of gut microbiome to mitigrate spurious correlation](#subtopic6)<br>
2. [Machine Learning](#topic2)<br>
  2.1 [Microbiome-based machine learning models to predict childhood obesity trajectory](#subtopic7)<br>
3. [Genomic Bioinformatics](#topic3)<br>
  3.1 [Comparative genomics of Lactobacillus reuteri isolates from gut and sourdough](#subtopic8)<br>
<br/>
<br/>
<h2 id="identifier" class="heading2">
  🦠Microbiome Epidemiology <a name="topic1"></a>
</h2>
--- 

<h3 id="identifier" class="heading3">
  Impact of vitamin D supplements on infant gut microbiome<a name="subtopic1"></a>
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">Linear Regression</span>
  <span class="tag is-info">Logistic Regression</span>
  <span class="tag is-info">Cohort study</span>
  <span class="tag is-info">Data Reporting</span>
  <span class="tag is-info">R</span>
</div>  

<img src="images/proj1_canva2.png"/>

<p id="identifier" class="p">
In this project, my colleagues and I developed a multiple linear model to investigate the relationship between vitamin D use, fecal metabolites, and microbiota, adjusting for covariables. The project used a cohort dataset of 575 infants. Vitamin D use and some prenatal variables were extracted from questionnaires; fecal metabolites and microbiota data were a readout of the NMR spectrum and high-throughput DNA sequencing, respectively. 
</p>
<br/>
[![](https://img.shields.io/badge/PDF-Open_research_poster-B44F99?logo=PDF)](pdf/Poster_vitD_microbiome_david.pdf) 
[![](https://img.shields.io/badge/HTML-View%20artile-yellow)](https://www.mdpi.com/2218-273X/13/2/200)

---
<h3 id="identifier" class="heading3">
Gut microbiota variations between IBD versus healthy adults<a name="subtopic2"></a> 
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">Mixed-Effect Modeling</span>
  <span class="tag is-info">Data Transformation</span>
  <span class="tag is-info">Multiple Test Correction</span>
  <span class="tag is-info">MaAsLin2</span>
</div>  
  
<img src="images/proj2_canva.png"/>

<p id="identifier" class="p">
To detect taxa differentially abundant in IBD patients, I built a generalized mixed-effect model with MaAsLin2 package, considering repeated samples as a random-effect variable. The input metagenomic data and metadata were derived from the openly available IBD dataset of the integrated human microbiome project (iHMP). 
</p>
<br/>
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-1182C3?logo=GitHub)](html/maaslin2-IBD-microbiome.html) 

---
<h3 id="identifier" class="heading3">
Benchmarking algorithms on zero-excessive metagenome data<a name="subtopic3"></a>
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">Zero-Inflation Model</span>
  <span class="tag is-info">Zero-Hurdle Model</span>
  <span class="tag is-info">R</span>
</div>  

<img src="images/proj3_canva.png"/>

<p id="identifier" class="p">
Four statistical algorithms, zero-inflated negative binomial, zero-inflated Poisson, zero-hurdle negative binomial, and zero-hurdle Poisson have been proposed in the literature to treat excessive zeroness (i.e., zero inflation) in various datatype, including microbiome count data. I benchmarked the four algorithms using microbiome dataset from Human Microbiome Project. Furthermore, I evaluated the performance based on AIC and likelihood ratio test.  
</p>
<br/>
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](html/zero-inflated-models-mcirobiome.html) 

---

<h3 id="identifier" class="heading3">
Differential analysis of microbiota data with over-dispersion using edgeR package<a name="subtopic4"></a>
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">edgeR</span>
  <span class="tag is-info">Negative Binomial</span>
  <span class="tag is-info">Over-dispersion</span>
</div>  

<img src="images/image_overdispersion_david.png?raw=false"/> 

<p id="identifier" class="p">
The microbiome is often over-dispersed and zero-inflated invalidating assumptions of conventional statistical models. The negative binomial algorithm can address the over-dispersion issue inherent in microbiome count data. In this project, I detected differentially-abundant taxa in IBD patients using the edgeR package that implements negative binomial modeling. 
</p>
<br/>

[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](html/overdisp-zeroinflate-model.html) 

---

<h3 id="identifier" class="heading3">
Correlation network development for gut microbial taxa using SparCC<a name="subtopic5"></a> 
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">Network Correlation</span>
  <span class="tag is-info">SparCC</span>
  <span class="tag is-info">ggraph</span>
</div>  

<img src="images/sparcc_git_profile.jpg"/>

<p id="identifier" class="p">
Friedman and Alm developed SparCC to infer the correlation network between taxa from microbiome data, effectively dealing with compositionality. This project aims to demonstrate application of SparCC on a microbiome dataset, using Python and R language. 
</p>
<br/>

[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](https://davidzhao1015.github.io/sparcc-relative-corr2/#1_install_package)

---
<h3 id="identifier" class="heading3">
Proportionality of gut microbiome to mitigrate spurious correlation<a name="subtopic6"></a> 
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">Relative Correlation</span>
  <span class="tag is-info">propr</span>
</div> 

<img src="images/propr_profile.jpg"/> 
<p id="identifier" class="p">
Lovell and co-authors (Lovell et al. 2015) proposed the proportionality method for relative correlation, as a valid alternative to absolute correlation. This project, thus, focused on illustrating the proportionality analysis of microbiome data using propr package by Quiin. Consistenet with previous findings, I observed proportionality is a precise indicator of absolute correlation, although sensitivity is limited. 
</p>
<br/>
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](https://davidzhao1015.github.io/association_analysis_compositional/)

--- 
<br/>
<br/>
<h2 id="identifier" class="heading2">
🤖Machine Learning<a name="topic2"></a> 
</h2>
--- 
<h3 id="identifier" class="heading3">
Microbiome-based machine learning models to predict childhood obesity trajectory<a name="subtopic7"></a> 
</h3> 
<br/>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">Predictive Modelling</span>
  <span class="tag is-info">Random Forest</span>
  <span class="tag is-info">XGBoost</span>
  <span class="tag is-info">caret</span>
</div>  

<img src="images/fig3_proj1.png?raw=false"/>

<p id="identifier" class="p">
Knowing obesity risk earlier could help healthcare professionals manage children's weight more effectively. This project aims to use fecal microbiome data to predict future obesity risk with machine learning algorithms. Random Forest, XGBoost, GLMM, and Regularized Logistic classifiers were developed based on the data set of 2000+ infants. The optimal classifier achieved an AUC of 0.83 with a specificity of 73% and sensitivity of 85%. 
</p>
<br/>
[![](https://img.shields.io/badge/PDF-Open_presentation_slides-C6466B?logo=PDF)](pdf/PPT_predict-child-obesity_davidzhao.pdf)
[![](https://img.shields.io/badge/GitHub-View_on_GitHub-0476D0?logo=GitHub)](https://github.com/davidzhao1015/infant_microbiota_predict_obesity/blob/main/bmi_traj_pred_infant_microbiota.Rmd) 

---
<br/>
<br/>
<h2 id="identifier" class="heading2">
🧬Genomic Bioinformatics<a name="topic3"></a> 
</h2>
--- 
<h3 id="identifier" class="heading3"> 
Comparative genomics of Lactobacillus reuteri isolates from gut and sourdough<a name="subtopic8"></a>  
</h3> 
<br/>

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css">
<div class="tags">
  <span class="tag is-info">standalone BLAST toolkit</span>
  <span class="tag is-info">MEGA 5</span>
  <span class="tag is-info">MAUVE</span>
  <span class="tag is-info">KEGG server</span>
</div>

<img src="images/image_comparative-genomics.png?raw=false"/>

<p id="identifier" class="p">
In this project, our team analyzed the genomic adaption of strains from guts to sourdoughs. Using comparative genomics, we pinpointed particular genes under positive selection. In addition, I developed the in-house bioinformatic pipeline, detecting DNA variations among strains. 
</p>
<br/>
[![](https://img.shields.io/badge/PDF-Open_presentation_slides-C6466B?logo=PDF)](pdf/PPT_phd_david.pdf)  
