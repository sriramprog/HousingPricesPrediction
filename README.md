## HomeValue Forecast Project
This repository contains the code for a project that quantifies the relationship between neighborhood walkability and housing prices in Philadelphia. The project aims to analyze if higher walk scores correlate with increased property values while considering other factors such as crime rates and school scores.

## Key Code File
The code for this project is contained in a single Python script. Below is a brief overview of the steps taken and the corresponding functions. [View code here](https://github.com/sriramprog/HousingPricesPrediction/blob/main/Sriram%20Data%20Science%20Project%20Finalized%20Code.ipynb)

1. **Data Collection and Preprocessing**
- Dataset: Sourced from Kaggle's Philadelphia Real Estate dataset. The data includes information for 615 properties, with features such as price estimates, walk score, crime rate, and school scores.
Cleaning:
- Type conversion of variables to numeric types.
- Handling of missing values and invalid characters in columns like Zillow Estimate and Rent Estimate.

2.  **Feature Engineering**
- Binning: Binned Walk Score and Crime Rate into categories to explore how they impact housing prices.
- One-Hot Encoding: Categorical features (e.g., crime and walk score bins) are encoded for use in machine learning models.
- Min-Max Scaling: Scaled numerical features to a range of 0-1 for model consistency.

3. **Data Visualization**
- Frequency Distribution of Walk Score: Visualized to understand the most common walk score ranges in the dataset.
- Frequency Distribution of Zillow Price Estimates: Visualized to see the distribution of home prices.
- Correlation Matrix: A heatmap was created to explore correlations between various features, including walk score, crime rate, and home prices.

4. **Statistical Analysis**
- OLS Regression: Performed regression analysis to assess feature significance.
- Assumptions Testing:
  - Normality Test using Q-Q plot.
  - Linearity and Homoscedasticity Tests.
  - Multicollinearity Test using Variance Inflation Factor (VIF).

5. **Machine Learning Models**
- Model Comparison:
  - Lasso Regression: Achieved MAE of 26,587.
  - SVR: Achieved MAE of 56,756.
  - XGBoost: Achieved MAE of 25,796.
  - Random Forest Regression: Best performing with MAE of 20,991.
  
- K-Fold Cross-Validation: Tuned hyperparameters and optimized model performance using 10-fold cross-validation.

## How to Run the Code
1. Clone the repository: git clone https://github.com/sriramprog/HousingPricesPrediction.git
2. Install dependencies: Ensure you have all required libraries installed: pip install -r requirements.txt
3. Run the code:
- The script includes all steps, from data loading and preprocessing to training and evaluating models.
- To execute the script, run: python housing_prices_prediction.py
4. Visualize the output: The code generates visualizations and prints evaluation metrics, including Mean Absolute Error (MAE) for each model tested.

## References
For a detailed description of the project, including background, data preprocessing, model development, and results, please visit my [Notion Repository](https://prickle-individual-755.notion.site/Project-3-HomeValue-Forecast-13ef9c7e94308022b936e207084c642b).
