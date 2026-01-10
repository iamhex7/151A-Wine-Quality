# Wine Quality Analysis: A Physicochemical Perspective

## Overview
This project investigates the relationship between the physicochemical properties of red and white wines and their perceived quality ratings. Using a dataset of over 6,000 observations from the UC Irvine Machine Learning Repository, I developed a series of linear regression models to identify key quality drivers and explore how these relationships differ between wine types.

## Research Questions
* Which physicochemical properties are most strongly related to wine quality?
* Are there systematic differences in these relationships between red and white wines?

## Methodology

### Data Processing and Exploratory Data Analysis
* **Variable Transformation:** Analysis revealed that predictors such as residual sugar, chlorides, sulfur dioxide, sulfates, and volatile acidity exhibited significant right-skewed distributions. These were log-transformed to stabilize variance and improve linearity.
* **Wine Type Stratification:** Exploratory data analysis showed differences in the distribution of several predictors between red and white wines, indicating potential interactions between wine type and chemical variables.



### Model Specification
The final model was selected based on a systematic comparison of adjusted R-squared, AIC, and BIC. The selected model includes interaction terms that allow the effect of specific chemical properties to vary by wine type, balancing explanatory power with interpretability.

**Model Formulation:**
The final regression model relates wine quality to alcohol content, fixed acidity, pH, and the log-transformed versions of residual sugar, volatile acidity, chlorides, total sulfur dioxide, citric acid, and sulphates, along with their interactions with wine type.

### Model Diagnostics and Robustness
* **Linearity:** Residual plots confirmed that the linear approximation was reasonable with no apparent systematic patterns between residuals and fitted values.
* **Normality:** The normal Q-Q plot showed slight deviations in the tails, which were considered acceptable given the large sample size of over 6,000 observations.
* **Homoscedasticity:** Scale-location plots indicated a moderate degree of heteroscedasticity. To ensure valid inference, the analysis was conducted using heteroscedasticity-robust (HC3) standard errors.
* **Influence:** Cook's distance and leverage diagnostics confirmed that no observations exerted undue influence on the fitted model.



## Main Findings
* **Alcohol:** Alcohol content is the strongest positive predictor of wine quality, consistent with empirical wine science findings.
* **Interaction Effects:** Significant interaction effects were observed for residual sugar, volatile acidity, sulfur dioxide, and sulfates, indicating that red and white wines respond differently to these chemical attributes.
* **Predictive Power:** The inclusion of interaction terms significantly improved model fit compared to baseline pooled models, as evidenced by lower AIC and higher adjusted R-squared values.

## Tools Used
* **Language:** R
* **Libraries:** tidyverse (ggplot2, dplyr, tidyr, purrr, stringr), broom, ggfortify, sandwich, lmtest
* **Techniques:** Ordinary Least Squares (OLS), Feature Transformation, Interaction Modeling, HC3 Robust Standard Errors, Model Diagnostics (Cook's D, Leverage, Q-Q Plots)

## License and Terms of Use
Copyright 2025 Hex Wu, Jingzhi Zhang, Martin Yang. All rights reserved.

**Important Notice:**
This project is shared for portfolio and demonstration purposes only. Under no circumstances may this work, its text, code, or results be plagiarized, copied, or cited without explicit written permission from the authors.
