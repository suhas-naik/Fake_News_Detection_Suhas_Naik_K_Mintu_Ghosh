# Fake News Detection
## Suhas Naik K & Mintu Gosh
 
 
 
### Fake News Detection Report
### Objective
The objective of this project is to develop a Semantic Classification model. We utilize the Word2Vec method to extract semantic relationships from news text and train supervised models to categorize text based on its meaning rather than just syntax. This project demonstrates how understanding textual meaning helps in making more accurate and efficient decisions. 
Business Objective 
The spread of fake news has become a major challenge in the digital age. With the overwhelming number of news articles published daily, distinguishing between credible and misleading information is increasingly difficult. Automatic fake news detection systems are necessary to reduce misinformation and protect public trust. 
In this assignment, the goal is to build a Semantic Classification model using Word2Vec and supervised learning models to classify news articles as true or fake. 
 
### Data Preparation 
Two datasets were provided: True.csv and Fake.csv. 

Each dataset contained three columns: 
•	title: Title of the news article 

•	text: Full text of the news article 

•	date: Date of publication 

Shapes of the datasets: 

•	True News: (21417, 3) 
•	Fake News: (23502, 3) 

Additional Processing: 
•	A new column news_label was added: 
o 	1 for True news o 	0 for Fake news 

•	Both datasets were concatenated after adding the news_label column. 

•	Missing values were handled by dropping rows with null entries. 
 
### Text Preprocessing
The following preprocessing steps were applied: 

•	Converted text to lowercase. 

•	Removed text inside square brackets. 

•	Removed punctuation. 

•	Removed words containing numbers. 

•	Removed extra whitespace. 

Further, lemmatization was applied using spacy, where only nouns (POS tags NN and NNS) were retained to preserve the essential meaning of the articles. 
  
### Train-Validation Split 
The concatenated dataset was split into: 

•	70% training data 

•	30% validation data using train_test_split from scikit-learn. 
  
  
### Observations: 
•	"Trump" was the most frequent word in both true and fake news datasets. 

•	Fake news articles contained more multimedia-related words such as "image", "video", and "medium". 

•	True news articles contained more formal government-related words like "government", "state", "official". 
 
### Feature Extraction
Feature vectors were generated using the Word2Vec model. This allowed capturing semantic relationships between words rather than relying solely on syntax. 
 
Model Training and Evaluation Logistic Regression: 
•	Accuracy: 0.90 
•	Precision: 0.90 
•	Recall: 0.90 
•	F1 Score: 0.90 Decision Tree: 
•	Accuracy: 0.82 
•	Precision: 0.83 
•	Recall: 0.79 
•	F1 Score: 0.81 Random Forest: 
•	Accuracy: 0.91 
•	Precision: 0.91 
•	Recall: 0.89 
•	F1 Score: 0.90 
 
### Insights and Outcomes 
Patterns Observed in True and Fake News: 

•	The dataset appeared well-balanced, so no synthetic data generation like SMOTE was necessary. 

•	Significant differences were observed through n-gram analysis, with different dominant words between true and fake articles. 

•	Removing stop words and applying noun-focused lemmatization improved model performance and efficiency. 

### Model Performance:
•	Logistic Regression performed extremely well, achieving high accuracy and precision with a simple model structure. 

•	Decision Tree underperformed compared to logistic regression but could potentially be improved with more hyperparameter tuning. 

•	Random Forest delivered strong results similar to logistic regression and could further benefit from fine-tuning. 

### Model Chosen: 
•	Logistic Regression was chosen as the final model. 

•	It is a simple and computationally inexpensive model, making it efficient for both deployment and future retraining without requiring extensive hardware resources. 
 
