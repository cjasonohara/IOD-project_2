# IOD-project_2
# FOOD ACCESS FOR SENIORS - EDA & Machine Learning Models
## JUNE 2024

## Project Overview
This was the second of four projects designed to reinforce and demonstrate my learning as part of the Institute of Data, Data Science & AI program. I chose to use a real-world dataset (USDA Food Access Research Atlas) to help a fictional Social Security Administration (SSA) allocate their funds in areas that would have the biggest impact for seniors experiencing food access issues. Further, I worked to create a machine learning model that would help SSA provide a tool to help local governments and municipalities allocate funds across their respective micro-areas.

- **Link to Dataset used (2019 version, updated 04/27/21):** https://www.ers.usda.gov/data-products/food-access-research-atlas/download-the-data/
- **Link to project presentation media:** 

### Objectives
- **Stakeholder Problem/Question**: Work to understand, clarify, and simplify the business problem that needs to be solved.
- **Data Science Problem**: Translate that business problem into a Data Science problem.
- **Summary of Data Used**: Provide a summary of the data used and why.
- **EDA and Data Visualization**: Explore, analyze and visualize the dataset in a way that either supports or does not support the business question.
- **Visualization of Feature Engineering**: Demonstrate the process used to engineer the features and the results.
- **Model Selection & Execution**: Select the best models to help provide predictive results.
- **Summary of Results**: Summarize and show the results.
- **Conclusion**: What were the lessons learned and what would the next steps be.

## Project Components

### Stakeholder Problem
- **SSA - Granted additional funding to spend on increasing food resources in the US.**
- **Priorities**: 1. Help as many, as quickly as possible. 2. Process must be repeatable for any locality.
- **Business Question**: Where can we allocate funds that have the biggest impact for seniors to access additional food sources?

### Data Science Problem
- **Access within .5 miles as Predictor**: Highest correlation between population and Owned Housing Units in a geographical area.

### Data Used
- **USDA Food Access Research Atlas**: https://www.ers.usda.gov/data-products/food-access-research-atlas/download-the-data/

### Data Cleaning & EDA
- Broke data table into three csv files for workability.
- Leveraged the Look Up Table to understand the data, reference codes and to help guide through next steps.
- Parsed data into different blocks (5, total) Block 1 = roll up data; Blocks 2-5 = Distance from a Supermarket, along with detail relating to that distance.
- Worked through correlation and PCA analysis
- Visualized using Folium and Google API for location lat/long conversion and mapping.
- Refocused and continued to look for correlations with 'core' features like population and owned housing units.
- Identified predictor in 'Seniors .5 miles away from Supermarket'
- Converted target variable to binary representation to assist with modeling.

### Model Selection and Results
- Selected various models based on relevancy to type of data (census) used.
- Started with Logistic Regression, Decision Tree, Random Forest and Dec Tree w/ Cross Validation - Perfect scores on last 3 - Overfitting?
- Determined that the feature I used to develop the binary target was allowing the models to easily learn/predict. Removed and ran models again.
- Scores better reflected in the results. Also added ensemble models.
- Random Forest was the strong performer at 88% - enough for a 'guide'. Why? Less prone to overfitting, good on large datasets and non-linear relationships.

### Summary of Results
- Able to identify where to spend for biggest impact - Seniors > .5 mile from supermarket & in the 75th percentile of the population for that area.
- Also able to create a model to duplicate identification by locality using population, housing and ethnicity variables.

### Conclusion
- **Continue to Add Features**: Time was a factor. I would add more features across all buckets to gain more insight. More can be done with this dataset.
- **Ask "Why Did This Work?"**: Asking why something worked is just as important as asking why something didn't work. Adding in a logic check helps to reinforce findings with stakeholders.
