# DSA210 Project Final Report - Kaan Önal 32019

## Analyzing the Relationship Between Sleep Patterns and Cognitive Performance

---

## Introduction

The relationship between sleep and cognitive performance has been a subject of scientific interest for decades, with implications for academic performance, workplace productivity, and overall well-being. This project investigates how personal sleep patterns affect cognitive function, specifically reaction time performance, through a systematic data-driven approach spanning 78 days of self-collected data.

This study examines the correlation between various sleep metrics (sleep duration, sleep timing, wake-up time) and cognitive performance as measured by Human Benchmark reaction time tests. By combining statistical analysis with machine learning techniques, the project aims to provide actionable insights into optimizing sleep schedules for better cognitive efficiency.

The analysis employs both traditional statistical hypothesis testing and modern machine learning approaches to evaluate whether sleep patterns significantly influence cognitive performance, and to identify which sleep-related factors are most predictive of reaction time outcomes.

---

## Data Description

### Dataset Overview

The dataset consists of 78 daily records collected from March 14, 2025, to May 30, 2025, representing a comprehensive three-month self-tracking study. Each record contains:

- **Date**: Daily tracking period  
- **Sleep Time**: Time of sleep 
- **Wake-Up Time**: Time of awakening  
- **Total Sleep Duration**: Calculated sleep duration in hours  
- **Human Benchmark Score**: Reaction time performance (milliseconds)

### Data Characteristics

- **Sample Size**: 78 observations  
- **Sleep Duration Range**: 4.35 - 10.00 hours  
- **Reaction Time Range**: 256 - 412 milliseconds  
- **Average Sleep Duration**: 7.5 hours  
- **Average Reaction Time**: 318 milliseconds  

The data collection methodology ensured consistency by measuring reaction time immediately upon waking to minimize confounding factors such as caffeine consumption, physical activity, or time-of-day effects.

---

## Exploratory Data Analysis

### Key Insights from Data Exploration

#### 1. Sleep Duration Distribution

The sleep duration data shows a roughly normal distribution with most nights falling between 6-9 hours. There are notable instances of both very short sleep (under 5 hours) and extended sleep (over 9 hours), providing good variance for analysis. The distribution suggests typical adult sleep patterns with occasional deviations due to lifestyle factors.

#### 2. Reaction Time Variability

Reaction time scores exhibit considerable day-to-day variability, ranging from 256ms to 412ms. This 156ms range represents significant cognitive performance variation, suggesting that multiple factors beyond sleep may influence daily cognitive function. The variability provides an opportunity to identify whether sleep patterns contribute meaningfully to this variation.

#### 3. Sleep Pattern Categories

Through feature engineering, sleep patterns were categorized into:

- **Sleep Duration**:  
  - Very Short (<5h)  
  - Short (5–7h)  
  - Optimal (7–9h)  
  - Long (>9h)  
- **Sleep Timing**:  
  - Very Early (<2 AM)  
  - Early (2–4 AM)  
  - Normal (4–6 AM)  
  - Late (>6 AM)  
- **Wake Timing**:  
  - Early (<9 AM)  
  - Normal (9–12 PM)  
  - Late (12–3 PM)  
  - Very Late (>3 PM)

#### 4. Temporal Patterns

Analysis of weekend vs. weekday performance shows minimal differences in both actual and predicted reaction times, suggesting that sleep's impact on cognitive performance is consistent regardless of the day type. This finding supports the robustness of the sleep-cognition relationship analysis.

---

## Hypothesis Testing

### Primary Hypothesis: Sleep Duration and Cognitive Performance

- **H₀** (Null): There is no significant correlation between total sleep duration and reaction time performance 
- **H₁** (Alternative): There is a significant correlation between total sleep duration and reaction time performance

#### Methodology
- **Pearson correlation** test was conducted to evaluate the linear relationship between total sleep time (hours) and Human Benchmark reaction time scores (milliseconds). This statistical approach provides a direct measure of the strength and direction of any linear association.

#### Results
- **Correlation Coefficient**: r = -0.173  
- **P-value**: 0.122 
- **Statistical Significance**: Not significant (p > 0.05)

**Interpretation**: The analysis failed to reject the null hypothesis, indicating no statistically significant correlation between sleep duration and reaction time performance. The weak negative correlation (r = -0.173) suggests that longer sleep duration has virtually no predictive relationship with better (lower) reaction times. The high p-value (0.122) confirms that this relationship could easily be due to random chance rather than a true underlying association.

---

## Machine Learning Analysis

### Objective

The machine learning component aimed to build predictive models to estimate reaction time performance based on engineered sleep features. By evaluating multiple algorithms, the analysis sought to determine whether complex, non-linear relationships exist between sleep patterns and cognitive performance that simple correlation analysis might miss.

### Feature Engineering

To enhance model performance and capture nuanced sleep patterns, several engineered features were created:

- **Categorical Sleep Variables**: Sleep timing, wake timing, and duration categories
- **One-Hot Encoding**: Transformation of categorical variables into binary indicators
- **Temporal Features**: Weekend/weekday indicators and day-of-week variables
- **Sleep Quality Indicators**: Sleep debt calculations and consistency metrics
- **Rolling Averages**: 3-day and 7-day sleep duration averages to capture consistency effects

### Models Evaluated

| Model           | MAE   | RMSE  | R² Score |
|----------------|-------|-------|----------|
| Random Forest  | 30.96 | 39.53 | -0.2847  |
| Linear Regression | 33.65 | 41.24 | -0.3982  |
| K-Neighbors    | 33.29 | 42.24 | -0.4669  |
| Decision Tree  | 42.67 | 52.98 | -1.3072  |

### Interpretation

- **Random Forest** (best performing model)
  
Achieved the lowest RMSE (39.53) and highest R² (-0.2847) among all models
The negative R² value indicates that the model performs worse than simply predicting the mean reaction time for all observations
Despite being the "best" model, it demonstrates that sleep features are not predictive of reaction time performance

- All models produced negative R² scores, which is a significant finding indicating that:

**No Predictive Relationship**: Sleep patterns do not reliably predict cognitive performance
**Model Limitations**: The engineered features, despite their sophistication, fail to capture meaningful relationships
**Baseline Comparison**: Simply predicting the average reaction time (318ms) would outperform all trained models

- The consistently poor model performance across different algorithms suggests that reaction time variability is driven by factors not captured in sleep data alone. This could include:

External environmental factors
Non-sleep related cognitive influences (stress, motivation, etc.)

---

## Results and Discussion

### Key Findings

- **No significant correlation** between sleep duration and cognitive performance (r = -0.071, p = 0.66)
- **Poor predictive models** — all worse than the mean
- **High variability** likely driven by non-sleep factors
- **Sleep categories** show no clear trends

### Scientific Implications

- Simple sleep metrics are insufficient
- Individual differences likely dominate
- Reaction time may not be sensitive enough

### Practical Implications

- Prioritize **consistency and quality** over raw duration
- Don’t expect drastic gains from more sleep alone
- More comprehensive measurements are needed for clearer insights

---

## Conclusions and Recommendations

### Primary Conclusions

- **Sleep duration alone is not predictive** of cognitive performance
- The relationship is **complex and multifactorial**
- **Individual variability** plays a major role

### Recommendations for Future Research

- **Extended Tracking**:
  - >6 months, multiple cognitive metrics, sleep quality details  
- **Feature Improvements**:
  - Sleep regularity, chronotype, environmental context  
- **Methodological Enhancements**:
  - Controlled sleep schedules, physiological data, multiple daily tests  
- **Personalized Models**:
  - Optimal durations per individual, genetic sleep predispositions

### Practical Applications

- Maintain consistent sleep schedules  
- Monitor subjective quality, not just hours  
- Avoid universal sleep rules in workplaces or schools  

---

## Final Insights

This study challenges assumptions about sleep’s role in daily cognition. While sleep matters, **simple duration metrics** don't capture the full picture. Personalization and more sophisticated methods are key to uncovering meaningful patterns.

---

## References

- **Human Benchmark Platform** – Reaction time tests  
- **Python Libraries** – Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn  
- **Statistical Methods** – Pearson correlation, hypothesis testing  
- **ML Models** – Random Forest, Decision Tree, Linear Regression, KNN  
- **EDA Tools** – One-hot encoding, categorical binning, rolling averages  
- **Visualization** – Matplotlib, Seaborn  
