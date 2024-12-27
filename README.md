# IPO Prediction Project

This project investigates the factors influencing the success of Initial Public Offerings (IPOs) using machine learning techniques. The goal is to develop a model that can predict whether an IPO will experience positive listing gains.

## Data

The project utilizes a dataset named `IPO_2024.csv`. This dataset is assumed to contain relevant features about IPOs, such as issue size, subscription rates, and listing gain percentages.

## Methodology

1. **Data Preprocessing**
   - Load the CSV data using pandas.
   - Handle missing values (e.g., dropping rows or imputation).
   - Convert the 'Date' column to datetime format.
   - Create a new binary target variable `Listing Gain Profit` to indicate positive listing gains.

2. **Exploratory Data Analysis (EDA)**
   - Analyze the distribution of features like issue size, listing gains, and subscription rates.
   - Visualize the relationship between features and the target variable using plots (e.g., scatter plots, violin plots).
   - Calculate the correlation matrix to explore feature relationships.

3. **Feature Engineering**
   - Create new features if necessary (e.g., total subscription value).
   - Scale numerical features using StandardScaler.

4. **Machine Learning Modeling**
   - Split the data into training and testing sets.
   - Train two machine learning models:
      - Logistic Regression: A baseline model for classification.
      - Gradient Boosting Classifier: A more powerful ensemble model for potentially better performance.
   - Use GridSearchCV to find the best hyperparameters for the Gradient Boosting model.
   - Evaluate model performance using metrics like accuracy, precision, recall, ROC AUC, and F1 score.
   - Visualize feature importances for both models to understand the relative contribution of features to the predictions.

5. **Model Evaluation**
   - Analyze the confusion matrix to assess the model's performance in identifying positive listing gains.
  

## Results

This project successfully developed and evaluated machine learning models to predict the success of Initial Public Offerings (IPOs) in the Indian stock market. Two models were implemented: Logistic Regression and Gradient Boosting.

### Model Performance

**Logistic Regression:**

- Accuracy: 0.732
- Precision: 0.873
- Recall: 0.716
- ROC AUC: 0.742
- F1 Score: 0.787

**Gradient Boosting:**

- Accuracy: 0.804
- Precision: 0.833
- Recall: 0.896
- ROC AUC: 0.748
- F1 Score: 0.863

### Feature Importance

Both models highlighted the importance of **Subscription_QIB** as a key predictor of IPO success. This suggests that the level of subscription by Qualified Institutional Buyers (QIBs) is a strong indicator of an IPO's potential for positive listing gains.

### Confusion Matrix Analysis

The confusion matrices for both models provide further insights into their performance. The Gradient Boosting model demonstrates a higher number of correct predictions for both "No Profit" and "Profit" cases, indicating better overall performance.

### Conclusion

This project shows that machine learning can be used to predict the success of Initial Public Offerings (IPOs). The Gradient Boosting model performed better than the Logistic Regression model in predicting whether an IPO would be successful. However, it is important to remember that these models are not perfect and should not be used as the only source of information when making investment decisions.

### Disclaimer

This project is for educational purposes only. It is not intended to provide financial advice. Investing in the stock market involves risks, and you should always consult with a qualified financial advisor before making any investment decisions.
