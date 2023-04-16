# Machine Learning Analysis on Credit Risk Classification

<img width="848" alt="Screenshot 2023-04-16 at 10 55 13 AM" src="https://user-images.githubusercontent.com/106120403/232321423-9a14f2d8-3c86-4feb-b8f5-f412ca62c886.png">

I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the credit worthiness of borrowers.

## Split the data set into testing and training sets using train_test_split

Dropped Loan Status (the output variable) from the x variable and created a y variable with only Loan Status

Features (x variables) used for this analysis:
loan_size,	interest_rate,	borrower_income,	debt_to_income,	num_of_accounts,	derogatory_marks,	total_debt

Using Logistics Regression Model to fit the data with a random state of 1

<img width="586" alt="Screenshot 2023-04-16 at 11 02 50 AM" src="https://user-images.githubusercontent.com/106120403/232321820-0f1f9794-4af4-4474-9236-ba34553e9655.png">

1. How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

The logistic regression model predicts the healthy loan labels with an precision of 1, which captures all the positive predictions. This predicts the healthy loans correctly 100% of the time. On the other hand, high-risk loan labels have high recall, which amounted to 0.91 which is good because it identifies 91% of all high risk loans correctly. The logistics regression model has an accuracy of 0.99. Both have good F1 score which means that model accurately captures/predicts the dataset

Used the RandomOverSampler module from the imbalanced-learn library to resample the data

Used the LogisticRegression classifier and the resampled data to fit the model and make predictions

<img width="586" alt="Screenshot 2023-04-16 at 11 05 26 AM" src="https://user-images.githubusercontent.com/106120403/232321988-0afee82e-4bc7-4ebf-b79b-fcaf0bcb17d3.png">

2. How well does the logistic regression model, fit with oversampled data, predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

The oversampled model provides a better result on the recall high risk loans (i.e. increased from 0.91 to 0.99).
Both the healthy loans and high risk loans have high recalls of 0.99. This means that it identifies correctly 99% of the healthy and high risk loans.
