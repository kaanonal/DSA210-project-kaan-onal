## Final Project Overview

The relationship between sleep and cognitive performance has been a subject of scientific interest for decades, with implications for academic performance, workplace productivity, and overall well-being. This project investigates how personal sleep patterns affect cognitive function, specifically reaction time performance, through a systematic data-driven approach spanning 78 days of self-collected data.

This study examines the correlation between various sleep metrics (sleep duration, sleep timing, wake-up time) and cognitive performance as measured by Human Benchmark reaction time tests. By combining statistical analysis with machine learning techniques, the project aims to provide actionable insights into optimizing sleep schedules for better cognitive efficiency.

The analysis employs both traditional statistical hypothesis testing and modern machine learning approaches to evaluate whether sleep patterns significantly influence cognitive performance, and to identify which sleep-related factors are most predictive of reaction time outcomes.

## Objectives

1. **Understand Sleep-Cognition Relationship:**  
   Evaluate whether common assumptions about the sleep-cognition link hold true through a systematic self-study.

2. **Explore Predictive Sleep Features:**  
   Identify which aspects of sleep behavior (timing, consistency, duration) might predict cognitive function.

3. **Apply Analytical Techniques:**  
   Use both hypothesis testing and machine learning to model reaction time based on sleep features.

4. **Contribute to Scientific Inquiry:**  
   Present findings—positive or negative—to contribute to a nuanced understanding of how sleep affects mental performance.

## Data Set

### Dataset Overview

The dataset consists of 78 daily records collected from March 14, 2025, to May 30, 2025, representing a comprehensive three-month self-tracking study. Each record contains:

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

The data collection methodology ensured consistency by measuring reaction time immediately upon waking to minimize confounding factors such as caffeine consumption, physical activity, or time-of-day effects.

## Tools and Technologies

- **Python**: For scripting and data analysis  
- **Pandas & NumPy**: Data manipulation and statistics  
- **Matplotlib & Seaborn**: Visualization of sleep-reaction trends  
- **Scikit-learn**: Machine learning modeling  
- **Human Benchmark**: Reaction time test platform  
- **Statistical Libraries**: For correlation analysis and hypothesis testing  

## Analysis Plan

### Exploratory Data Analysis

1. **Sleep Duration Distribution**  
   Shows a roughly normal distribution (6-9 hours typical); outliers on both ends provide variability.

2. **Reaction Time Variability**  
   Day-to-day scores range widely (256ms–412ms); suggests multiple factors at play.

3. **Sleep Pattern Categories**  
   - **Duration**: Very Short (<5h), Short (5-7h), Optimal (7-9h), Long (>9h)  
   - **Sleep Timing**: Very Early (<2 AM), Early (2-4 AM), Normal (4-6 AM), Late (>6 AM)  
   - **Wake Timing**: Early (<9 AM), Normal (9-12 PM), Late (12-3 PM), Very Late (>3 PM)

4. **Temporal Patterns**  
   No major differences between weekday/weekend reaction times; sleep-cognition effects remain stable.

### Hypothesis Testing

- **H₀**: No correlation between sleep duration and reaction time  
- **H₁**: Longer sleep improves reaction time  

- **Method**: Pearson correlation  
- **Result**:  
  - Correlation Coefficient: r = -0.071  
  - P-value: 0.66428  
  - **Interpretation**: No significant correlation (p > 0.05). Weak negative relationship likely due to chance.

### Machine Learning Analysis

**Goal**: Build predictive models for reaction time based on sleep features.

**Feature Engineering**:
- Sleep timing/duration/wake-time categories
- One-hot encoding
- Temporal flags (weekend, day-of-week)
- Rolling averages
- Sleep debt and consistency

**Models Evaluated** (Train/Test = 80/20 split):

| Model            | MAE   | RMSE  | R² Score  |
|------------------|-------|-------|-----------|
| Random Forest    | 30.96 | 39.53 | -0.2847   |
| Linear Regression| 33.65 | 41.24 | -0.3982   |
| K-Neighbors      | 33.29 | 42.24 | -0.4669   |
| Decision Tree    | 42.67 | 52.98 | -1.3072   |

**Findings**:
- All models had **negative R²**, meaning worse than baseline (mean prediction).
- **No predictive relationship** found between sleep patterns and reaction time.
- **Random Forest** was best among the models but still ineffective.

### Result Summary

- **No strong correlation** between sleep and reaction time.
- **Sleep categories** (short, optimal, long) didn't show consistent performance differences.
- **Models failed** to predict accurately, reinforcing the weak sleep-cognition relationship.

## Conclusion

### Key Findings

- No significant correlation between sleep duration and cognitive performance.
- Machine learning models failed to find meaningful patterns.
- Cognitive performance likely affected more by individual or external factors than by sleep alone.

### Scientific Implications

- Duration may not be enough—sleep **quality**, **stages**, and **individual needs** might be more relevant.
- Reaction time may not be sensitive enough or is influenced by too many variables.

### Practical Implications

- Focus on **consistency and quality**, not just duration.
- Results caution against expecting major performance improvements solely from more sleep.
- Consider **personalized sleep strategies** and **comprehensive metrics**.

## Recommendations

1. **Longer Tracking Periods**  
   6+ months of data may reveal subtler trends.

2. **Multiple Cognitive Measures**  
   Use additional tasks (e.g., memory, attention) to diversify evaluation.

3. **Advanced Sleep Metrics**  
   Include quality, regularity, and environment (light, noise, etc.).

4. **Personalization**  
   Develop individualized models to understand unique sleep-performance dynamics.

## Final Insights

This study demonstrates that simplistic assumptions about sleep and performance can be misleading. While sleep clearly affects cognition, its influence may not be easily captured through duration alone or simple tests. Nuanced analysis, personalized modeling, and broader data are required to truly understand and optimize the sleep-cognition connection.

## References

- Human Benchmark Platform – Used for standardized reaction time measurements  
- Python Data Analysis Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn  
- Statistical Methods: Pearson correlation analysis, hypothesis testing frameworks  
- Machine Learning Algorithms: Random Forest, Decision Tree, Linear Regression, K-Nearest Neighbors  
- Feature Engineering Techniques: One-hot encoding, categorical variable transformation, rolling averages  
- Data Visualization: Matplotlib and Seaborn for exploratory data analysis and results presentation
