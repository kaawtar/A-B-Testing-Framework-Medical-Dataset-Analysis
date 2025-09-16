# A/B Testing Framework – Medical Dataset Analysis

## Project Overview
This project presents a **Python framework** to run and analyze A/B tests on medical data.  
It evaluates whether changes in treatment (Group B) outperform the control group (Group A).

**Applications:**  
- Clinical studies and treatment evaluation  
- Marketing campaigns  
- UX/Product experiments  


## Objective
Develop a **reusable Python framework** to:  
- Compute **descriptive statistics** for continuous and binary metrics  
- Perform **hypothesis testing** (t-test for continuous, Chi-square for categorical)  
- Calculate **confidence intervals** and **effect sizes**  
- Generate **visualizations** for easy interpretation  
- Enable **data-driven decision-making**


## Key Features
- Handles **continuous** (`Units_per_dose`) and **binary** (`improvement`) metrics  
- Provides **p-values, confidence intervals, and effect sizes**  
- Generates **bar charts, boxplots, and CI plots**  
- Outputs **clear decision recommendations**  
- Modular design for **reusable A/B testing analysis**


## Workflow

### 1. Data Preparation
- Load and clean the dataset (`ID`, `Med`, `Admin Date`, `Units`)  
- Define groups: **Group A (control)** and **Group B (treatment)**  

### 2. Descriptive Statistics
**Continuous Metric (`Units_per_dose`):**  
- Group A: mean = 302.55, std = 655.67, n = 1802  
- Group B: mean = 0.60, std = 0.99, n = 219  

**Binary Metric (`improvement`):**  
- Group A: proportion improved = 49.7%, n = 1802  
- Group B: proportion improved = 45.2%, n = 219  

### 3. Hypothesis Testing
- **Continuous Metric (t-test):** t = 6.81, p < 0.001 → **significant difference**  
- **Binary Metric (Chi-square):** χ² = 1.42, p = 0.234 → **not significant**  

### 4. Confidence Intervals & Effect Size
**Continuous Metric:**  
- Cohen’s d = 0.49 (moderate effect)  
- 95% CI for mean difference: 271.68 – 332.23  

**Binary Metric:**  
- 95% CI for improvement rate:  
  - Group A: 47.4 – 52.0%  
  - Group B: 38.6 – 51.8%  

### 5. Decision Making
- **Units:** Statistically significant difference between groups  
- **Improvement:** No significant difference → Group B treatment does not clearly outperform Group A  

### 6. Visualization
- Bar charts for proportions  
- Boxplots for continuous metrics  
- Confidence interval plots to visualize differences  


## Deliverables
- **Jupyter Notebook** with step-by-step explanations  
- **Reusable Python class/functions** for A/B testing  
- **Plots** visualizing group comparisons  
- **Summary report** with statistics, p-values, confidence intervals, and effect sizes  


## Conclusion
- **Units (`Units_per_dose`)**: Group A received substantially higher dosages than Group B, confirmed by t-test and Cohen’s d.  
- **Improvement:** No statistically significant difference between groups, suggesting that Group B does not lead to better outcomes under current conditions.  
- Recommendations: **subgroup analysis**, **longer follow-up**, or **adjusted dosages** for further evaluation.  



