# Financial Returns Forecasting and Portfolio Performance Evaluation

This project focuses on forecasting the financial returns of assets using various regression models and machine learning techniques. The goal is to predict asset returns and optimize portfolio performance using models like linear regression, neural networks, and ensemble methods. 

## Project Overview

The project involves:

1. **Forecasting Financial Returns**: I used historical data of financial assets to forecast their returns from 2013 to 2022.
2. **Regression Models**: Several regression models were applied, including:
   - **Linear Regression with L2 Loss**
   - **Linear Regression with Huber Loss**
   - **OLS-3+H Regression Model**
   - **Elastic-Net Regression**
3. **Machine Learning Models**:
   - **Principal Component Regression (PCR)**
   - **Partial Least Squares (PLS) Regression**
   - **Neural Networks** (3, 4, and 5 layers)
   - **Random Forest**
   - **Gradient Boosting Machines (GBM)**
4. **Expanding Window Approach**: Implemented an expanding window strategy to predict returns on financial assets from 2013 to 2022.
5. **Portfolio Construction**: Constructed two types of portfolios:
   - **Mobile Portfolio**: Adjusts dynamically based on performance and market conditions.
   - **Fixed Portfolio**: Maintains a constant asset allocation over the evaluation period.
6. **Portfolio Performance Metrics**: Evaluated the performance of each model with three additional metrics:
   - **Drawdowns**: Measures the decline from the peak value of the portfolio.
   - **Turnover**: Calculates the rate of asset changes in the portfolio.
   - **Max1Mloss**: Tracks the maximum loss in any rolling 1-month period.

## Methodology

### Data

The historical data used to forecast asset returns includes market prices and financial indicators from 2013 to 2022. The data was preprocessed and cleaned before being split into training and testing datasets for each model.

### Models

1. **Linear Regression (L2 & Huber Loss)**: Classic linear regression models with two loss functions:
   - **L2 Loss** (Squared Error) for standard linear regression.
   - **Huber Loss** for robustness to outliers.
   
2. **OLS-3+H Regression**: A specialized ordinary least squares model with enhancements to improve its forecasting accuracy.

3. **Elastic-Net Regression**: A regularized regression model that combines L1 (Lasso) and L2 (Ridge) penalties to improve predictive accuracy and reduce overfitting.

4. **PCR and PLS**:
   - **PCR (Principal Component Regression)**: A dimensionality reduction technique used for regression.
   - **PLS (Partial Least Squares)**: Focuses on modeling the relationships between the inputs and outputs using latent variables.

5. **Neural Networks**: Implemented feed-forward neural networks with varying numbers of layers (3, 4, and 5) to capture complex non-linear relationships in the data.

6. **Ensemble Models**:
   - **Random Forest**: An ensemble of decision trees to improve predictive performance.
   - **Gradient Boosting**: An ensemble technique that builds trees sequentially to correct errors made by previous trees.

### Expanding Window Strategy

For the time-series prediction, an expanding window approach was used to train models on increasing subsets of data (starting from 2013) and then predict returns for the subsequent years up until 2022. This approach simulates real-world conditions, where models are retrained periodically with new data.

### Portfolio Construction and Performance Evaluation

- **Mobile Portfolio**: This portfolio adjusts its asset allocation based on performance predictions and market conditions.
- **Fixed Portfolio**: The allocation remains constant over the entire period.
- **Performance Metrics**: To assess the effectiveness of each model, I defined and calculated three key metrics:
  - **Drawdowns**: Measures the largest peak-to-trough loss during the period.
  - **Turnover**: Indicates the frequency of changes in the asset allocation.
  - **Max1Mloss**: Identifies the maximum loss over any one-month period.

## Results and Evaluation

The performance of each model was evaluated based on the prediction accuracy of asset returns as well as portfolio metrics. The models were tested for their ability to minimize drawdowns, reduce turnover, and avoid significant losses during volatile periods.

## Conclusion

This project demonstrates the power of machine learning and statistical models in forecasting financial returns and optimizing portfolio management. By applying various regression models and machine learning techniques, I was able to predict asset returns and assess the performance of mobile and fixed portfolios. The additional metrics provided further insights into the risk and stability of each model’s portfolio.

## Future Work

- Exploring more advanced models such as deep reinforcement learning for dynamic portfolio optimization.
- Extending the analysis to include other factors, such as macroeconomic indicators or sentiment analysis, to improve the accuracy of financial predictions.

## Dependencies

- Python 3.x
- Libraries: numpy, pandas, scikit-learn, seaborn, keras, tensorflow, xgboost, lightgbm, matplotlib, statsmodels
