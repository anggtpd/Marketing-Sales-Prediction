# Marketing Sales Prediction
This project contains linear regression models to predict sales based on marketing spend on **TV** and **Radio**.

## Project Structure

## Dataset
The dataset includes the following columns:
- TV – Marketing spend on TV ads
- Radio – Marketing spend on radio ads
- Social Media – Marketing spend on social media ads
- Influencer – Spend on influencer marketing
- Sales – Resulting sales figures

## Preprocessing
- Dropped irrelevant columns (Radio, Social Media, Influencer for TV model; TV, Social Media, Influencer for Radio model)
- Handled missing values by imputing with the mean
- Split the data into training and test sets (80/20 split)
- Scaled the data for better model performance

## Modeling
- Used Linear Regression from scikit-learn
- Trained the model on the training set
- Predicted on the test set

## Results
TV Model:
- R² Score: 0.99 → Very high, possibly indicating overfitting
- Mean Absolute Error (MAE): 2.78
- Mean Squared Error (MSE): 63.12
- Root Mean Squared Error (RMSE): 7.94
![TV Sales Prediction](../output_tv_sales.png)

Radio Model:
- R² Score: 0.75 → Strong correlation but not overfitting
- Mean Absolute Error (MAE): 36.41
- Mean Squared Error (MSE): 2069.43
- Root Mean Squared Error (RMSE): 45.49

## Conclusion
- The TV model’s R² score of 0.99 indicates that it explains nearly all the variance in sales, but it may be overfitting the training data.
- The Radio model’s R² score of 0.75 shows a strong correlation without overfitting, suggesting it generalizes better.
- Potential improvements include trying other regression models (e.g., Ridge, Lasso) and feature engineering.
