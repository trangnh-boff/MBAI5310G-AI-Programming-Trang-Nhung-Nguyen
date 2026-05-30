# Assignment 4: FreshCart Plus Decision Tree Classification

## Business Problem

FreshCart Plus is an online grocery delivery and subscription-based retail business. Customers pay for a membership to receive benefits such as free or reduced-fee delivery, priority delivery windows, exclusive discounts, and personalized grocery recommendations.

The business problem is to predict whether customers are likely to renew their membership. This is important because customer retention helps FreshCart Plus reduce churn, protect subscription revenue, and use retention offers more effectively.

## Dataset Used

The dataset used in this assignment is the FreshCart subscription decision tree dataset.

Each row represents one FreshCart Plus customer. The dataset includes customer profile, membership information, purchase behaviour, service experience, app engagement, and risk factor variables.

The target variable is:

- `Renewed_Membership`

The target variable has two values:

- `Yes` = the customer renewed the membership
- `No` = the customer did not renew the membership

The `Customer_ID` column was not used as an input feature because it is only an identifier.

## Machine Learning Model Used

The machine learning model used in this assignment is a Decision Tree Classifier.

The Decision Tree model was used because it is suitable for a binary classification problem and can help explain which features are important when predicting customer renewal.

## Main Evaluation Results

The Decision Tree model results were:

- Training Accuracy: 0.8750
- Testing Accuracy: 0.8333
- Accuracy: 0.8333
- Precision for Renewed_Membership = Yes: 0.8571
- Recall for Renewed_Membership = Yes: 0.3529
- F1-score for Renewed_Membership = Yes: 0.5000

The confusion matrix was:

| Actual / Predicted | Predicted No | Predicted Yes |
|---|---:|---:|
| Actual No | 54 | 1 |
| Actual Yes | 11 | 6 |

The training accuracy and testing accuracy were reasonably close. The overfitting gap was about 0.0417, so the model did not show a strong sign of overfitting.

## Key Business Insights

The model can help FreshCart Plus identify customer renewal patterns and support retention decisions.

For the No-renewal class, the recall was 0.98, meaning the model identified most customers who actually did not renew. This is useful because FreshCart Plus wants to find at-risk customers before they leave.

The most important features with meaningful importance were:

- Monthly_Orders
- App_Sessions_Per_Month
- Late_Deliveries_Last_3M
- Delivery_Rating

These features can help FreshCart Plus understand how customer activity, app engagement, and delivery experience are related to membership renewal. For example, customers with fewer monthly orders, lower app engagement, more late deliveries, or lower delivery ratings may need customer support follow-up or service recovery before the renewal date.

## One Limitation

One limitation is that the dataset may not include every real world reason why customers renew or leave. Customer renewal may also depend on income, product quality preferences, family schedule, competitor pricing, or personal reasons. Because of this, the model should be used as a decision-support tool, not as the only basis for business decisions. Human judgment is still important when deciding which customers should receive retention support.

