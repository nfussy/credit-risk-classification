# credit-risk-classification

## Overview of the Analysis
<ul>
  <li>The purpose of this analysis was to test a logistic regression model on a dataset to see if it can predict healthy or high-risk loans.</li>
  <li>The information that was provided in the dataset:</li>
    <ul>
      <li>loan_status: `0` for healthy loans and `1` for the high-risk ones.</li>
      <li>loan_size: the quantity that was loaned out.</li>
      <li>interest_rate: the interest rate at which the loan was assigned.</li>
      <li>borrower_income: the income of the individual receieving the loan.</li>
      <li>debt_to_income: ratio calculated from the amount of debt compared to the income.</li>
      <li>number_of_accounts: the number of accounts held by the borrower.</li>
      <li>derogatory_marks: unspecified; likely account overdrafts, bounced checks, etc.</li>
      <li>total_debt: the amount of debt the borrower carries.</li>
    </ul>
  <li>The status of the loan is a boolean value: `0` for healthy loans and `1` for the high-risk ones.</li>
</ul>

### Stages of the Machine Learning Process
<ul>
  <li>Assigned the column of 'loan_status' to the variable 'y' and the remainder of the dataset was assigned to the variable 'x'.</li>
  <li>Using the train_test_split from sklearn.model_selection, the dataset is split into two groups:</li>
    <ul>
      <li>75% assigned to the training model.</li>
      <li>25% assigned to the testing model.</li>
    </ul>
  <li>The training variables are fitted to a Logistic Regresssion model and the model is trained.</li>
  <li>The testing variables are then fitted to the trained Lineal Regression model.</li>
  <li>A confusion matrix and classification report are then created to display the results of the test and to check the model's accuracy.</li>
</ul>

## Results

<ul>
  <li>Accuracy: 99%</li>
  <li>Precision:</li>
  <ul>
    <li>`0` Healthy Loans: 1.00</li>
    <li>`1` High-Risk Loans: 0.85</li>
  </ul>
  <li>Recall:</li>
  <ul>
    <li>`0` Healthy Loans: 0.99</li>
    <li>`1` High-Risk Loans: 0.95</li>
  </ul>
</ul>

## Summary
The logistic regression model performed rather well with an overall accuracy of 99%; however, it seems slightly skewed due to the perfect 100% predictions of healthy loans, versus it's 89% F1 score in determining the amount of high-risk loans.

With a total of 25000 high-risk loans, it would mean that 2750 high-risk loans were missed. This tends to point to there being additional factors that would affect the ability of these individuals to be less risky.
