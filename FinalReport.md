# DSA210 Project Final Report

## Analyzing the Relationship Between Sleep Patterns and Cognitive Performance

---

## Introduction

The relationship between sleep and cognitive performance has been a subject of scientific interest for decades, with implications for academic performance, workplace productivity, and overall well-being. This project investigates how personal sleep patterns affect cognitive function, specifically reaction time performance, through a systematic data-driven approach spanning 78 days of self-collected data.

This study examines the correlation between various sleep metrics (sleep duration, sleep timing, wake-up time) and cognitive performance as measured by Human Benchmark reaction time tests. By combining statistical analysis with machine learning techniques, the project aims to provide actionable insights into optimizing sleep schedules for better cognitive efficiency.

The analysis employs both traditional statistical hypothesis testing and modern machine learning approaches to evaluate whether sleep patterns significantly influence cognitive performance, and to identify which sleep-related factors are most predictive of reaction time outcomes.

---

## Data Description

### Dataset Overview

The dataset consists of 78 daily records collected from March 14, 2025, to May 30, 2025. Each record contains:

- **Date**: Daily tracking period  
- **Sleep Time**: Time of sleep onset  
- **Wake-Up Time**: Time of awakening  
- **Total Sleep Duration**: Calculated sleep duration in hours  
- **Human Benchmark Score**: Reaction time performance (milliseconds)

### Data Characteristics

- **Sample Size**: 78 observations  
- **Sleep Duration Range**: 4.35 - 10.00 hours  
- **Reaction Time Range**: 256 - 412 milliseconds  
- **Average Sleep Duration**: ~7.5 hours  
- **Average Reaction Time**: ~318 milliseconds  

Measurement consistency was ensured by recording reaction time immediately upon waking.

---

## Exploratory Data Analysis

### Key Insights from Data Exploration

#### 1. Sleep Duration Distribution
- Roughly normal distribution centered between 6-9 hours.
- Some nights <5 hours or >9 hours — good variance for analysis.

#### 2. Reaction Time Variability
- Range: 256ms to 412ms (156ms variation).
- Indicates high day-to-day variability.

#### 3. Sleep Pattern Categories
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
- Weekday vs. weekend performance showed minimal differences.
- Sleep’s cognitive effect appears consistent across days.

---

## Hypothesis Testing

### Primary Hypothesis: Sleep Duration and Cognitive Performance

- **H₀**: No significant correlation between total sleep duration and reaction time  
- **H₁**: Significant correlation exists

#### Methodology
- **Pearson correlation** between total sleep time and reaction time.

#### Results
- **Correlation Coefficient**: r = -0.071  
- **P-value**: 0.66428  
- **Statistical Significance**: Not significant (p > 0.05)

**Interpretation**: No statistically significant relationship. The weak negative correlation suggests longer sleep duration is not predictive of improved reaction time.

---

## Machine Learning Analysis

### Objective

To build models predicting reaction time based on sleep-related features.

### Feature Engineering

- Categorical variables (sleep duration, timing)
- One-hot encoding
- Temporal features (weekday/weekend)
- Sleep quality indicators (sleep debt, consistency)
- Rolling averages (3-day, 7-day)

### Models Evaluated

| Model           | MAE   | RMSE  | R² Score |
|----------------|-------|-------|----------|
| Random Forest  | 30.96 | 39.53 | -0.2847  |
| Linear Regression | 33.65 | 41.24 | -0.3982  |
| K-Neighbors    | 33.29 | 42.24 | -0.4669  |
| Decision Tree  | 42.67 | 52.98 | -1.3072  |

### Interpretation

- **Random Forest** performed best but still had **negative R²**, indicating worse performance than predicting the mean.
- All models underperformed, suggesting:
  - Sleep features are not predictive
  - Significant influence from external factors (stress, environment, physiology, etc.)

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
