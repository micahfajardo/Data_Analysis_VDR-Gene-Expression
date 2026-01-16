# Analysis of Genomic and Clinical Data: VDR Expression in Melanoma

## 📋 Project Overview
This project investigates the molecular landscape of the Vitamin D Receptor (VDR) in melanoma patients. Using R, I processed genomic datasets (Copy Number Alterations and RNA-Seq) and clinical data to identify how VDR genomic status correlates with gene expression and patient demographics
> The datasets used in this project are available upon request. 

---

## 🛠️ Technical Skills Demonstrated

### 1. Bioinformatics Data Wrangling
* **Data Importation and Cleaning:** Loaded large-scale genomic matrices inTXT for CNA and mRNA expression. I utilized `pivot_longer` to convert wide-format genomic data into long-format tidy data and `stringr` to regex-strip patient ID suffixes (to be able to merge it in relation to other tables).

### 2. Statistical Analysis
* **Normality Testing:** Automated Shapiro-Wilk tests across multiple groups to determine the appropriateness of non-parametric methods
* **Non-Parametric Comparisons:** Implemented Kruskal-Wallis for multi-group variance and Wilcoxon Rank-Sum tests for pairwise comparisons.
* **Multiple Testing Correction:** Applied the False Discovery Rate (FDR) method to adjust p-values for genomic scale comparisons. <br>
**Libraries used:** `dplyr`, `ggplot2`, `tidyverse`, `ggpubr`, `stringr`, `rstatix`, `readr`
  
---

## 📊 Key Results

### VDR Copy Number vs. Expression
* **Observation:** As the GISTIC copy number increases from -1 (loss) to 2 (amplification), there is a statistically significant increase in VDR mRNA expression.
 
### Clinical Correlations
* **Gender:** No significant difference in VDR expression was found between Male and Female cohorts.
* **Vital Status:** Patients who were "Dead" vs "Alive" showed a marginal trend but did not meet the standard 0.05 significance threshold for expression.

---

## 🧬 Future Research Direction

Using the Muralidhar et al. datasets, we can develop a multivariable prognostic model incorporating VDR copy number, VDR expression, and key pathological features derived from biopsy. Before model construction, the data must first show that VDR markers meaningfully improve prediction of disease-free status.If proven, the following research questions should be addressed to support the model's validity:
* Do VDR copy number variation and VDR expression predict Disease-Free Status independently of tumor stage (T, N, M components of the AJCC Group Stage)?
* Can VDR markers stratify patients within AJCC Stage II or Stage III into distinct high- and low-risk groups?
* Is the association between VDR markers and recurrence risk modified by primary tumor characteristics(i.e. Clark level and tumor site)?
