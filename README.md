# Wine Quality Analysis: A Physicochemical Perspective

## Overview
This project investigates the relationship between the physicochemical properties of red and white wines and their perceived quality ratings. [cite_start]Using a dataset of over 6,000 observations from the UC Irvine Machine Learning Repository [cite: 8, 38][cite_start], I developed a series of linear regression models to identify key quality drivers and explore how these relationships differ between wine types[cite: 7, 9].

## Research Questions
* [cite_start]Which physicochemical properties are most strongly related to wine quality? [cite: 9]
* [cite_start]Are there systematic differences in these relationships between red and white wines? [cite: 10]

## Methodology
### Data Processing and EDA
* [cite_start]**Skewness Correction:** Variables such as residual sugar, chlorides, and sulfur dioxide exhibited significant right-skewness and were log-transformed to stabilize variance and improve linearity[cite: 14, 15, 31].
* [cite_start]**Feature Engineering:** Analysis of distributions revealed that red and white wines often follow different chemical profiles, prompting the inclusion of interaction terms between wine type and chemical predictors[cite: 16, 20].

### Model Specification
[cite_start]The final model (Model D) was selected based on a systematic comparison of AIC, BIC, and adjusted R-squared values[cite: 23]. [cite_start]This model balances explanatory power with interpretability[cite: 24].

**The Final Regression Equation:**
$$quality = \beta_0 + \beta_1 alcohol + \beta_2 \log(sugar) + \dots + \beta_k (\log(predictor) \times type_{white}) + \epsilon$$
[cite_start][cite: 27, 28, 30]

### Model Diagnostics and Robustness
* [cite_start]**Linearity:** Residual plots confirmed that the linear approximation was reasonable[cite: 37].
* [cite_start]**Normality:** Q-Q plots showed slight deviations in the tails but were deemed acceptable given the large sample size[cite: 38].
* [cite_start]**Homoscedasticity:** Scale-location plots indicated moderate heteroscedasticity[cite: 39]. [cite_start]This was addressed by conducting inference using heteroscedasticity-robust (HC3) standard errors[cite: 40].
* [cite_start]**Influence:** Cook's distance and leverage diagnostics confirmed no observations exerted undue influence on the model[cite: 41].

## Main Findings
* [cite_start]**Alcohol:** Alcohol content is the most significant positive predictor of wine quality[cite: 45, 57].
* [cite_start]**Acidity:** Quality is strongly associated with acidity-related measures[cite: 57].
* [cite_start]**Interaction Effects:** Red and white wines respond differently to chemical attributes[cite: 46]. [cite_start]Specifically, the impact of residual sugar, volatile acidity, sulfur dioxide, and sulfates varies significantly depending on the wine type[cite: 47, 48].

## Tools Used
* Language: R
* Libraries: tidyverse, broom, ggfortify, car, sandwich, lmtest

## License and Terms of Use
Copyright (c) 2025 Hex Wu, Jingzhi Zhang, Martin Yang. [cite_start]All rights reserved. [cite: 3]

**Important Notice:**
This project is shared for portfolio and demonstration purposes only. Under no circumstances may this work, its text, code, or results be plagiarized, copied, or cited without explicit written permission from the authors.
