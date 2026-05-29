# Assignment 4-1: PayFlow Invoice Late Payment Prediction

## Business Problem

PayFlow Business Solutions is a B2B financial operations company that helps small and medium-sized businesses manage invoicing, payment collection, accounts receivable, payment reminders, online payment portals, and financial reporting dashboards.

The business problem is that late invoice payments can create cash-flow problems for businesses. When customers pay late, companies may struggle to pay suppliers, manage payroll, invest in operations, and plan future growth.

The goal of this project is to use machine learning to predict whether an invoice is likely to be paid late.

## Dataset Used

The dataset used in this assignment is:

`payflow_invoice_late_payment_dataset.xlsx`

Each row represents one invoice issued to a business customer.

The target variable is:

`Late_Payment`

A value of `Yes` means the invoice was paid late.  
A value of `No` means the invoice was paid on time.

The input features include customer information, invoice amount, payment terms, prior late payments, average days to pay, dispute flag, reminder count, online portal use, and credit score band.

`Invoice_ID` was removed because it is only an identifier and does not represent meaningful business behavior.

## Machine Learning Model Used

The machine learning model used in this project is:

`Decision Tree Classification Model`

The model was evaluated using:

- Confusion matrix
- Accuracy
- Precision
- Recall
- F1-score
- Training accuracy
- Testing accuracy

## Main Evaluation Results

Metric Result: 

- Training Accuracy: 1.0000 
- Testing Accuracy: 0.5694 
- Accuracy: 0.5694 
- Precision: 0.5152 
- Recall: 0.5313 
- F1-score: 0.5231 

The confusion matrix showed:

Result Type Count:

- True Negative: 24 
- False Positive: 16 
- False Negative: 15 
- True Positive: 17 

## Key Business Insights

The Decision Tree model can help PayFlow identify invoices that may be at risk of late payment.

Recall for `Late_Payment = Yes` is especially important because PayFlow wants to identify as many truly risky invoices as possible before they become overdue.

The model showed signs of overfitting because the training accuracy was 100.00%, while the testing accuracy was only 56.94%.

Important features such as invoice amount, prior late payments, average days to pay, reminder count, and days since last order can help PayFlow decide which invoices may need early reminders, account manager support, or closer monitoring.

## One Limitation

One limitation is that the dataset is simplified and may not include all real-world factors that affect payment behavior. Real payment behavior may depend on customer financial stress, contract terms, approval workflows, seasonal business cycles, economic conditions, or customer relationships. Because of this, the model should support human judgment and should not replace staff review.
