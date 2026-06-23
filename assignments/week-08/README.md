# Assignment 8: NLP Text Classification of Public Library Service Requests

## Dataset Description

This project uses the **Public Library Service Request Classification Dataset**, which contains 120 patron service requests submitted to RiverCity Public Library. The dataset includes information such as request details, patron information, communication channels, and request categories. The main text data is stored in the PatronMessage column, which contains the messages submitted by library patrons.

## Target Variable

The target variable is **RequestCategory**, which represents the type of service request submitted by a patron. The categories include:

* Book_Availability
* Digital_Access
* Event_Registration
* Facility_Issue
* Staff_Help
* Study_Space

The objective is to automatically classify patron messages into the correct request category.

## Model Used

Text preprocessing techniques including lowercasing, punctuation removal, stopword removal, tokenization, and lemmatization were applied to the text data. The cleaned text was converted into numerical features using TF-IDF (Term Frequency–Inverse Document Frequency).

A Multinomial Naive Bayes classifier was then trained to predict the request category.

## Main Evaluation Results

The model achieved excellent performance on the testing dataset:

* Accuracy: 100%
* Precision: 1.00
* Recall: 1.00
* F1-Score: 1.00

The confusion matrix showed that all test records were classified correctly.

## Main Business Interpretation

The model successfully predicts the category of library service requests based on patron messages. This can help RiverCity Public Library automatically route requests to the appropriate department, reduce manual processing time, and improve response efficiency.
Text analysis showed that words such as library, staff, study, book, branch, and event appeared frequently in patron messages. This suggests that library resources, study spaces, staff assistance, and events are common topics of concern among patrons.

## Limitation of the Model

One limitation of this project is the relatively small dataset size of 120 records. Although the model achieved perfect accuracy on the test data, its performance may differ when applied to larger and more diverse real-world patron requests. Additional data would help improve the model's robustness and generalizability.
