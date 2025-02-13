# DS4002-Project 1: Phishing Email Sentiment Analysis 
### Group Leader: Will Mayer
### Group 20: Ethan Banerjee, Camila Gutierrez

## (1) Software and Platform
Software type: Python 

Packages: 
* Pandas Package
* NLTK (Natural Language Toolkit) Package  
* Matplotlib Package
* Numpy Package
* Wordcloud Package 
* Vader Sentimental Analysis Package
* Scikit-learn

Platform: Mac/Windows
## (2) A Map of Documentation
This repository contains the contents necessary to implement our sentiment analysis which consists of 3 main folders:

DATA FOLDER: 
* **raw.csv**: Our raw dataset containing email_text (str) and email_type (str)
* **sentiment.csv**: Our dataset with sentiment analysis scores. These calculations take a long time so we've saved them here as a benchmark. This file contains email_text, email_type, and four values representing sentiment intensity scores.
* **email.parquet**: Our final established dataset after transforming email_text to numerical representation using TF-IDF (Term Frequency-Inverse Document Frequency) vectorization. We used unigrams and bigrams (one and two-word phrases).

OUTPUT FOLDER: 
* **confusion_matrix.png**:
* **email_dist.png**
* **email_length.png**
* **phishing_wordcloud.png**
* **safe_wordcloud.png**
* **sentiment_distribution.png**


SCRIPTS FOLDER:
* **basic_eda.ipynb**: This script reads in the raw.csv for exploratory data analysis of the relationship between the email text and email type columns. Distribution of email types, email text length, and most common words are investigated through figures.   
* **make_data.ipynb**: This script transforms raw.csv to email.parquet, adding sentiment analysis scores, and transforming email_text to numerical representations. This file takes a long time to run, so we recommend you use the email.parquet we've provided and skip straight to analysis.ipynb.
* **analysis.ipynb**: This script uses email.parquet to train a logistic regression model to predict whether an email is spam or not. This script measures the accuracy of the model and generates scripts and tables for our output folder.

## (3) Result Replication

### In order to replicate the results of our study, you must follow these steps:
If you want to fully recreate our dataset, you can run make_data.ipynb. This file takes a long time to run, and we recommend using the email.parquet we've provided and skip straight to analysis.ipynb. 

Recreating our dataset requires the following dependencies:
- numpy
- pandas
- scikit-learn
- nltk and VADER

To recreate our analysis, run analysis.ipynb using email.parquet.

## (4) References
[1] N. Kumaran, “Spam does not bring us joy—ridding Gmail of 100 million more spam messages with TensorFlow,” Google Workspace Blog. Accessed: Jan. 30, 2025. [Online]. Available: https://workspace.google.com/blog/product-announcements/ridding-gmail-of-100-million-more-spam-messages-with-tensorflow

[2] Oklahoma State University Stillwater, “Malicious Emails and Financial Scams - Oklahoma State University.” Accessed: Jan. 30, 2025. [Online]. Available: https://it.okstate.edu/resources/security-education/malicious-emails.html

[3] K. Bostoganashvili, “Spam Filters Explained [2025].” Accessed: Jan. 30, 2025. [Online]. Available: https://mailtrap.io/blog/spam-filters/

[4] S. Sayyafzadeh, M. Weatherspoon, J. Yan, and H. Chi, “Securing Against Deception: Exploring Phishing Emails Through ChatGPT and Sentiment Analysis,” in 2024 IEEE/ACIS 22nd International Conference on Software Engineering Research, Management and Applications (SERA), 2024, pp. 159–165. doi: 10.1109/SERA61261.2024.10685564.

[5] “VADER sentiment analysis (with examples) | Hex,” *hex.tech*. https://hex.tech/use-cases/sentiment-analysis/vader-sentiment-analysis/  
