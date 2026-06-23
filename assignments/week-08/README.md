# Assignment 8: NLP and Text Classification 

## Dataset Description

This project uses the **Public Library Patron Requests Dataset**, which contains 120 patron messages submitted through different library channels such as email, chat, website forms, mobile apps, and front desk interactions. Each record includes a patron message along with information such as city, branch, patron type, request category, and priority level.

## Target Variable

The target variable is **RequestCategory**.

The categories include:

* Digital_Access
* Study_Space
* Facility_Issue
* Staff_Help
* Event_Registration
* Book_Availability

The goal is to automatically classify patron messages into the correct request category.

## Model Used

A **Multinomial Naive Bayes** classification model was used.
Text data was converted into numerical features using **TF-IDF (Term Frequency–Inverse Document Frequency)** before training the model.

## Main Evaluation Results

The model achieved:

* Accuracy: **100% (1.00)**
* Precision: **1.00**
* Recall: **1.00**
* F1-Score: **1.00**

The confusion matrix showed that all test records were correctly classified.

## Main Business Interpretation

The model can automatically categorize incoming library requests based on the text of the patron message. This can help library staff quickly route requests to the appropriate department, reduce manual work, and improve response times. Text analysis also showed that common words such as *library*, *staff*, *study*, *book*, and *event* frequently appeared in patron messages, indicating that patrons often contact the library about facilities, resources, and services.

## Limitation of the Model

A limitation of this project is the relatively small dataset size (120 records). The model achieved perfect accuracy on the test set, but its performance may decrease when applied to larger and more diverse real-world patron messages that contain different wording or topics.

