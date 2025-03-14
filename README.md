# DSA210-project-kaan-onal
## Project Overview
Over the next three months, I will analyze how my sleep schedule affects my cognitive performance, specifically my reaction
time. By recording my sleep start time, wake-up time, and total sleep duration, and correlating them with my Human Benchmark
reaction time test results, I aim to uncover whether sleep patterns influence cognitive function. Using statistical and
visualization techniques, I will explore patterns and test hypotheses to determine if longer or more consistent sleep improves
reaction time.

The plan is straightforward: track my sleep data, measure reaction time first thing in the morning, and analyze how different
sleep durations impact my cognitive performance. Ultimately, this project aims to provide actionable insights into optimizing
sleep schedules for better cognitive efficiency.

## Objectives

1. **Understand Sleep-Cognition Relationship**
    Examine the correlation between sleep duration, wake-up time, and reaction time performance.
    
2. **Identify Key Sleep Factors**
    Determine whether total sleep duration or consistency has a stronger impact on reaction time.

3. **Data-Driven Optimization**
    Use data analysis techniques to identify trends and provide insights into sleep habits that may enhance cognitive function.

4. **Apply Data Science Skills**
    Implement statistical modeling and regression analysis to derive meaningful conclusions about sleep’s impact on reaction
    time.
    
## Data Set

    The dataset for this project consists of three months of daily records. Here’s what I’ll be tracking:

    - **Date**: The specific day of the record
    - **Sleeping Time**: The time I went to bed
    - **Wake-Up Time**: The time I woke up
    - **Total Sleep Duration**: Difference between sleep start and wake-up time (hours)
    - **Reaction Time**: My Human Benchmark reaction time test result (ms) recorded immediately after waking up
    
    Data will be self-reported daily in an Excel sheet to ensure consistency and accuracy. Outliers caused by illness, sleep
    disruptions, or unusual circumstances will be flagged for review

## Tools and Technologies

    - **Python**: For data cleaning and statistical analysis
    - **Pandas**: To manipulate and preprocess data
    - **Matplotlib**: For visualizing sleep trends and reaction time correlations
    - **SciPy**: For hypothesis testing and regression analysis
    - **Human Benchmark**: The online platform used to measure reaction time performance
    
## Analysis Plan

1. **Data Collection**  
    - Import daily records into a Pandas DataFrame.
    - Handle missing values and ensure consistent formatting.

2. **Visualization**
    - Create scatter plots to visualize the relationship between sleep duration and reaction time.
    - Generate time series plots to examine reaction time trends over three months.
    - Compare reaction time distributions for different sleep durations.
    
3. **Hypothesis Testing**
    - **H₀**: Sleep duration and timing have no significant effect on cognitive performance.
    - **H₁**: Longer and more consistent sleep schedules improve reaction time.
    Conduct correlation analysis to determine if sleep duration is significantly related to reaction time.
    Use regression models to quantify the effect of sleep duration on reaction time.

4. **Trend Analysis & Prediction**
    - Investigate patterns in reaction time over time.
    - Identify if consistent sleep schedules lead to progressively faster reaction times.
    - Use linear regression to estimate how much additional sleep improves reaction time.
    
## Conclusion

    By the end of this project, I hope to answer the following questions:
    
    - Does sleep duration significantly affect reaction time performance?
    - Is reaction time improvement more influenced by total sleep duration or sleep schedule consistency?
    - Can small, data-driven adjustments to my sleep schedule lead to measurable improvements in cognitive performance?
    
This project is not just about understanding my own sleep habits—it’s about leveraging data science to optimize cognitive
function. The insights gained may contribute to better sleep scheduling strategies for improved mental performance in various
aspects of life, from academics to problem-solving efficiency.

