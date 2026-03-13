# Gait Asymmetry in Parkinson's Disease

Systematic evaluation of mathematical formulations of gait asymmetry applied to spatiotemporal gait parameters in Parkinson’s disease.

This repository contains the analysis pipeline used to compare different asymmetry metrics and to evaluate their clinical sensitivity in discriminating Parkinson’s disease (PD) from healthy subjects (HS) and in describing disease progression according to the Hoehn & Yahr (H&Y) scale.

---

# Background

Gait asymmetry is widely used as an indicator of altered bilateral motor control in Parkinson’s disease.  
However, the literature proposes multiple mathematical formulations to quantify asymmetry between left and right limbs. These metrics differ in their mathematical properties and often lead to heterogeneous results across studies.

This project aims to systematically evaluate commonly used asymmetry formulations and determine whether the choice of mathematical formulation or the gait variable itself plays a larger role in clinical sensitivity.

---

# Objectives

The study addresses three main questions:

1. **Mathematical redundancy**
   - Are different asymmetry formulas capturing the same underlying construct?

2. **Clinical discrimination**
   - Which asymmetry metrics best distinguish PD patients from healthy subjects?

3. **Disease progression**
   - Which metrics are most strongly associated with clinical progression according to the Hoehn & Yahr scale?

---

# Dataset

The dataset includes gait recordings from:

- **148 patients with Parkinson’s disease**
- **46 healthy subjects**

PD participants were distributed across **Hoehn & Yahr stages 1–3**.

Spatiotemporal gait parameters were collected using the **GAITRite® system** during comfortable walking.

Due to clinical data privacy restrictions, the dataset **cannot be publicly shared** in this repository.

---

# Gait variables analyzed

The following spatiotemporal parameters were analyzed:

- Stance time
- Step time
- Swing time
- Single support time
- Double support time
- Step length
- Stride length
- Stride time
- Stride velocity
- Base of support

---

# Asymmetry formulations

Twelve asymmetry metrics reported in the literature were evaluated.

These belong to three main mathematical families:

### Log-ratio formulations
- Absolute log ratio
- Signed log ratio
- Bounded log ratio

### Ratio-based metrics
- Simple ratio
- Ratio deviation
- Angular ratio transformation
- Symmetry ratio

### Difference-based metrics
- Absolute difference
- Event asymmetry
- Symmetry index
- Robinson symmetry index
- Signed normalized difference

These formulations differ in properties such as:

- symmetry under L/R inversion
- scale invariance
- boundedness
- distributional stability

---

# Analysis pipeline

The analysis is structured into five main steps.

### 1. Dataset overview
Exploration and preprocessing of gait data.

### 2. Mathematical structure of asymmetry metrics
Correlation analysis and PCA to evaluate redundancy between formulations.

### 3. PD vs Healthy comparison
Non-parametric comparison between PD and HS using:

- Mann–Whitney U test
- Cliff’s delta
- Bootstrap estimation of Cohen’s d

### 4. Association with disease progression
Correlation between asymmetry metrics and Hoehn & Yahr stage using:

- Spearman correlation
- Effect size ranking

### 5. Relative contribution of formula vs gait variable
Linear model evaluating the relative importance of:

- asymmetry formulation
- gait variable

in determining clinical sensitivity.

---

# Key findings

Main results of the analysis:

- Most asymmetry formulations are **mathematically redundant**, producing nearly identical effect sizes.
- Metrics based on **asymmetry magnitude** perform consistently better than signed formulations.
- **Temporal gait parameters** show the highest clinical sensitivity.
- **Stance time asymmetry** emerges as the most informative metric across analyses.
- The **gait variable** contributes more to clinical sensitivity than the specific mathematical formulation used.

---


---

# Requirements

Python environment used for the analysis:

- Python 3.11
- pandas
- numpy
- scipy
- scikit-learn
- statsmodels
- seaborn
- matplotlib

---

# Reproducibility

The repository contains the full analysis pipeline required to reproduce all statistical analyses and figures presented in the study.

To reproduce the results, the original dataset should be placed inside the `data/` folder.

---

# Authors

Dante Trabassi  
Collaborators: Marco Godi, Marica Giardini, Ilaria Arcolin

---

# Related work

This repository supports the abstract submitted to:

**Società Italiana di Riabilitazione Neurologica (SIRN)**

Title:  
*Comparison of asymmetry formulations for spatiotemporal gait parameters in Parkinson’s disease*

---

# License

This repository is shared for academic and research purposes.