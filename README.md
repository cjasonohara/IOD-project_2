# IOD-project_1
# FILM GENRE, BEST BET - Exploratory Data Analysis
## MAY 2024

## Project Overview
This was the first of four projects designed to reinforce and demonstrate my learning as part of the Institute of Data, Data Science & AI program. I chose a fictional problem of two independent filmmakers (my instructors) who approached me with the business question of which genre would be the 'safest' bet for them to pursue when developing their first feature film.

- **Datasets used are included in this repository**
- **Link to project presentation media:** 

### Objectives
- **Stakeholder Problem**: State the business problem/question to be solved.
- **Data Science Problem**: Translate the business problem into a Data Science problem.
- **Summary of Data Used**: Provide a summary of the data used and why.
- **Visualization of Data Wrangling**: Demonstrate the process used to wrangle the data and the results.
- **Visualization of Feature Engineering**: Demonstrate the process used to engineer the features and the results.
- **Visualization of EDA**: Demonstrate the process used for EDA and show the results.
- **Summary of Results**: Summarize and show the results.
- **Conclusion**: What were the lessons learned and what would the next steps be.

## Project Components

### Stakeholder Problem
- **First Feature Film**
- **Priorities**: Attract potential investors, appeal to wide audience, make money
- **Business Question**: What genre would be the 'safest' to pursue?

### Data Science Problem
- **Film Ratings as Predictor**: Used as investor benchmark, moviegoers also use
- **Is it a SMART Goal?**: Yes.
- **Agreed to Keep it Simple**

### Data Used
- **kaggle.com, IMDb Top 1000 Films, csv**: Right-sized, easy to work with, free
- **wikipedia.org, Unesco Institute for Statistics - Average Ticket Price**: Used US prices only; Where null, averaged between prior year & year following; Where null at start or end of data, used % increase/decrease for year(s) prior

### Data Wrangling
#### Kaggle Dataset
- Converted to Pandas DF
- Isolated main_genre
- Dropped unnecessary columns and null-value rows
- Retained columns needed for analysis
- Nulls were in the 16% ('Meta_score') and 17% ('Gross') range, respectively. Typically too high to drop
- Opted to replace 'Meta_score' nulls with mean and drop the 'Gross' nulls. Predictive Imputation for 'Gross' in the future?

#### UNESCO Dataset
- Converted to Pandas DataFrame
- Assumptions made before importing data
- Used US average ticket sale price only

### Feature Engineering
- After merging the two datasets, created a new column to determine # of tickets sold
- Used new column to help determine which genres would be most-likely to make money
- Using the mean, looked for comparisons between 'Main_genre' and 'IMDb_Rating', 'Meta_Score', 'Tickets_Sold', 'No_of_Votes'
- Compared against median to account for outliers, but it did not significantly change the outcome

### EDA Visualization
- Used Matplotlib to visualize the results
- Opted for a simple bar chart as that was the most effective in demonstrating the outcomes

### Summary of Results
- Able to demonstrate clear winners for each classification
- Also able to help determine which genres to stay away from for each classification

### Conclusion
- **Expand Dataset**: Not a big enough range; 'Top 1000', so data is already skewed
- **Explore Using Machine Learning**: Would yield better results for this type of exploration; Would provide more probabilistic outcomes vs stopping at EDA; goal would be to achieve a 'score' for each genre, based on a combination of features (vs just comparing against a single mean)
