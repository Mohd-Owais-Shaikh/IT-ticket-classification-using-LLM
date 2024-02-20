# IT Ticket Classification System
Refer Project Report for detailed documentation.

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

### Implementation
	### Description of Model Implementation  
		Traditional NLP Model Implementation 
			All our models follow the typical classification setup. The features are processed and as 
			mentioned in the TF-IDF section, we have one combined input feature of Complaints as a sparse matrix 
			and our target variable is the Products. Random forest is a powerful ensemble technique that iteratively 
			builds an additive model by minimizing the expected value of a given loss function, refining its 
			predictions with a series of weak learners, typically decision trees, to achieve high accuracy and 
			efficiency in various machine learning tasks. 

		BERT Large Language Model Implementation. 
			Further we fine-tuned an LLM from Hugging-Face called BERT-based-uncased to evaluate the AUC and improve classification. In this process, 
			the BERT based Uncased model for classification was fine-tuned on our dataset to produce a few shots 
			learning classification. Due to the compute resources limitation, we had to choose the retrain the model 
			over our modified dataset with 5 categories of classes instead of 17 which still required a lot of 
			computing resources. To implement this, we used Google Colab Pro with T4 GPU. It used 96.4 compute 
			units. The total training time was 3 hours. The model was pre-trained 7 billion parameters. For this approach, we 
			specifically chose the sequence classification model of Tensorflow python library which has been pre
			trained on book corpus, a dataset consisting of 11, 038 unpublished books and English Wikipedia. We 
			have trained the model on 30 epochs and the observed loss is negligible.
##### Classes

We have 5 different classes available in the target variable. They are listed below.
•	Credit card or prepaid card

•	Checking or savings account

•	Mortgage

•	Credit reporting, credit repair services, or other personal consumer reports

•	Credit card

•	Bank account or service

•	Debt collection

#### Results

BERT showed improvement in accuracy and performance by 7% over Logistic Regression.
Moving to the advantages of BERT, BERT provides contextual understanding by considering the entire 
context of the input text. This is particularly advantageous in understanding the nuanced language often 
present in IT tickets, leading to improved classification accuracy.The other advantage is BERT captures 
semantic representations of words and phrases, allowing the model to understand the meaning behind 
the text. This is crucial for handling IT tickets where specific terms and phrases may carry different 
meanings based on the context. 
On other hand, BERT models are computationally expensive, both in terms of training and 
inference. Logistic Regression, being a simpler model, is computationally more efficient. BERT models 
require substantial resources, including powerful GPUs, for efficient training and inference. Logistic 
Regression is more lightweight in terms of resource requirements. 
BERT Language Models exhibit superior performance in IT ticket classification due to their 
contextual understanding and semantic representations, they come with computational challenges. 
