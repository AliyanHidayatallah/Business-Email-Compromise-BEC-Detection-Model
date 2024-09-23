# Business Email Compromise (BEC) Detection Model

## Project Overview
This project focuses on detecting Business Email Compromise (BEC) by developing a machine learning model that classifies emails as either **ham** (legitimate) or **spam** (potential BEC threats). Using the **Enron email dataset**, the project leverages natural language processing (NLP) and machine learning techniques to identify patterns that distinguish between legitimate and phishing emails.

### Key Achievements:
- **Data Processing**: Cleaned and transformed a large dataset of emails.
- **Machine Learning**: Trained a Logistic Regression model for binary email classification.
- **Insightful Analysis**: Performed feature analysis to uncover patterns in spam emails, focusing on key terms frequently used in phishing attacks.
- **Hands-on Development**: Set up and managed the entire project within a virtual environment, using industry-standard tools.

## Dataset Overview
The **Enron email dataset** is one of the largest publicly available corpuses of email communications. The dataset contains thousands of emails, which are split into two categories:

- **Ham**: Legitimate emails sent within the organization.
- **Spam**: Emails that are classified as phishing attempts, potential BEC threats, or unwanted communications.

The dataset was used to train and evaluate the performance of the BEC detection model.

## Model Workflow

### Environment Setup
The development environment was established using **Anaconda**, which allowed for the creation of a virtual environment. This ensured that all necessary dependencies were isolated, making it easier to manage the project and its packages. I used **Jupyter Notebook** to interactively write and run the code, allowing for quick experimentation with different approaches.

### Data Cleaning and Preprocessing
To prepare the dataset for training, a preprocessor was developed to clean the raw text data. This involved:
- Removing non-alphabet characters (such as numbers and punctuation) to focus on the meaningful text.
- Converting text to lowercase, ensuring that word variations (e.g., "Click" vs. "click") were treated consistently.

These preprocessing steps were essential to enhance the quality of the data and improve the model's ability to identify patterns.

### Feature Extraction
The cleaned email content was converted into numerical vectors, representing word frequencies within the emails. This transformation was crucial for enabling the machine learning model to understand and learn from the data. The numerical vectors were created using word counts, allowing the model to identify key words or phrases often found in spam and legitimate emails.

### Model Training
The processed dataset was split into training and testing sets, with **80% used for training** the model and **20% reserved for testing**. A **Logistic Regression model**, which is widely used for binary classification tasks, was chosen. The model was trained to recognize patterns that indicate whether an email is spam or ham, based on the frequency of specific words within the email body.

### Model Evaluation
The trained model was evaluated on the test set to assess its performance. Key evaluation metrics included:
- **Accuracy**: The percentage of correct predictions, reflecting the overall performance of the model.
- **Precision, Recall, and F1-Score**: These metrics provided a more detailed analysis of the model’s ability to correctly classify spam and ham emails while minimizing false positives and false negatives.
- **Confusion Matrix**: A matrix was used to summarize the number of true positives, true negatives, false positives, and false negatives. This gave further insight into the model’s misclassifications and where improvements might be needed.

## Key Insights and Feature Analysis
After training and evaluating the model, a **feature analysis** was conducted to understand which words were most influential in determining whether an email was classified as spam or ham. By examining the model’s coefficients, we identified:

- **Top spam indicators**: Words such as "http", "free", and "click" were frequently associated with spam emails, especially those that involved phishing or fraudulent activity. These terms often appear in phishing links and scam promotions.
- **Top ham indicators**: Words like "re", "thank", and "attached" were commonly found in legitimate business communications.

This analysis highlighted key patterns in how spammers structure their emails and how legitimate email communication differs. These insights could be used to further refine email filtering systems, creating more robust protection against BEC attacks.

## Conclusion
This project successfully demonstrated the use of machine learning for detecting **Business Email Compromise (BEC)** threats. By analyzing a large corpus of emails and applying advanced data preprocessing and feature extraction techniques, the model achieved high accuracy in classifying emails. The feature analysis provided valuable insights into the specific patterns that distinguish spam from legitimate emails, further enhancing our understanding of phishing strategies.

The project offers a strong foundation for future developments in email security systems and could be expanded by incorporating more sophisticated models or additional datasets.
