# IT Ticket Classification System

## Team Members
- Owais Shaikh
- Ashutosh Joshi
- Amulya Potluri


### Introduction
In IT sector, most of the issues or bugs are usually solved through a ticketing system. There are several ways to raise a ticket. It can be through call using helpline number, informing the helpdesk, or filling a ticket form. Tickets are usually raised if there is anything wrong with the functionality, existing system, missing data, name change, components missing on a page, etc. These issues may be simple or complex but both types of issues can be fixed when a ticket is raised for them. Sometimes, one issue may end up creating one more issue. Issues are sometimes more complex to deal with if they are delayed. So, most of the IT support teams are usually loaded with lots of tickets. Each ticket has a specified team to resolve and time frame to be fixed. To tackle this challenge, we're considering using Natural Language Processing (NLP) technology, which enables computers to understand and process human language, to streamline ticket routing.


### Literature Survey

	Paramesh, Ramya, Shreedhara conducted research and developed a model for IT Ticket Classification. The model started with a collection of historical data on tickets which later followed a series of actions including pre-processing phase, vector representation, vector dimensionality reduction, model building and generating a response as output which says the team the ticket should be assigned. The dataset had 10,742 records and 18 different classes. This article also used bagging models to build the classifier model and considered accuracy, precision, recall, f-score as evaluation metrics. The proposed model in the article achieved an accuracy performance of LR, KNN, MNB and SVM are respectively 80.50%, 69.24%, 70.1% and 88.22% respectively.

Howard. J article proposed ULMFiT which is an effective transfer learning method that can be literally applied on any type of task in NLP. This primarily includes three stages discriminative fine-tuning, slanted triangular learning rates, and gradual unfreezing. These are used to retain the previous knowledge and train the model to achieve better predictions. Author utilized six widely studied datasets to deliver the significance of ULMFit. He used three common text classification tasks: sentiment analysis, question classification, and topic classification.
 
### Project Objective
The primary objective of this project is to create an advanced ticket classification system leveraging Large Language Models (LLMs). This system aims to provide substantial assistance to the IT support team by streamlining ticket and request handling. Its core functionality is to accurately route tickets to the appropriate department and to expedite issue resolution by ensuring that requests don't end up in the wrong hands.

### DATASET:

The data set is collected from Kaggle.
https://www.kaggle.com/datasets/venkatasubramanian/automatic-ticket-classification


Classes

We have 17 different classes available in the target variable. They are listed below.
•	Credit card or prepaid card

•	Checking or savings account

•	Mortgage

•	Credit reporting, credit repair services, or other personal consumer reports

•	Credit card

•	Bank account or service

•	Debt collection

•	Money transfer, virtual currency, or money service

•	Vehicle loan or lease

•	Consumer Loan

•	Student loan

•	Money transfers

•	Payday loan, title loan, or personal loan

•	Credit reporting

•	Other financial service

•	Prepaid card

•	Payday loan

Test Split: 20%
Train Split: 80%
