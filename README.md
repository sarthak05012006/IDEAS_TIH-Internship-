# IDEAS_TIH-Internship

🚀 ML Pipeline & Text Classification
A hands-on introduction to the Machine Learning pipeline and Natural Language Processing (NLP) using Python and Scikit-Learn.

This project demonstrates how raw data and text can be transformed into numerical features, used to train machine learning models, and evaluated using multiple classification metrics.

📌 Project Overview
The project covers three major stages of a machine learning workflow:
ML Problem-Solving Framework
Supervised vs. Unsupervised Learning

Features and targets

Handling missing values

Train/Test splitting

Text Data & Feature Engineering

Tokenization

Bag of Words (BoW)

TF-IDF

SMS Spam vs. Ham Classification

Multinomial Naive Bayes

Model Evaluation

Accuracy

Precision

Recall

F1-Score

Classification Report

Confusion Matrix

Logistic Regression comparison

The project is designed as a practical learning exercise where the code can be modified and experimented with using different text inputs.

🧠 What You'll Learn
Machine Learning Basics
Machine Learning allows computers to identify patterns from data instead of relying only on explicitly written rules.

The project introduces:

Supervised Learning: Learning from labeled data.

Unsupervised Learning: Finding patterns in unlabeled data.

Features (X): Input information used by a model.

Target (y): The value the model is trying to predict.

Train/Test Split: Separating data used for learning from data used for final evaluation.

Missing Values: Basic techniques for handling incomplete datasets.

📖 Text Feature Engineering
Machine learning models work with numerical data, so text must first be converted into numbers.

1. Tokenization
Breaking text into smaller units, usually words or tokens.

Example:

"I love machine learning"
can be represented as:

["I", "love", "machine", "learning"]
2. Bag of Words
Counts how frequently words appear in a collection of text.

The project uses Scikit-Learn's:

CountVectorizer()
3. TF-IDF
Term Frequency-Inverse Document Frequency gives higher importance to words that are more meaningful and less common across documents.

The project uses:

TfidfVectorizer()
📩 SMS Spam Classification
The main practical application is an SMS Spam vs. Ham classifier.

Ham = 0

Spam = 1

The dataset contains SMS messages labeled as either spam or ham.

The project loads the dataset from:

https://raw.githubusercontent.com/justmarkham/pycon-2016-tutorial/master/data/sms.tsv
ML Pipeline
SMS Messages
      ↓
Train/Test Split
      ↓
TF-IDF Feature Extraction
      ↓
Numerical Feature Matrix
      ↓
Machine Learning Model
      ↓
Predictions
      ↓
Evaluation
🤖 Models Used
Multinomial Naive Bayes
The primary model is:

from sklearn.naive_bayes import MultinomialNB

model = MultinomialNB()
model.fit(X_train_transformed, y_train)
It is used to classify SMS messages based on the numerical text features generated using TF-IDF.

Logistic Regression
The project also demonstrates how the machine learning model can be swapped with Logistic Regression while keeping the same feature-engineering pipeline.

from sklearn.linear_model import LogisticRegression

lr_model = LogisticRegression()
lr_model.fit(X_train_transformed, y_train)
This demonstrates an important ML workflow concept: the feature-processing pipeline can be reused with different models.

📊 Model Evaluation
Accuracy alone may not provide enough information, especially when classes are imbalanced.

The project evaluates the classifier using:

Accuracy
The percentage of predictions that are correct.

Precision
Among messages predicted as spam, how many are actually spam?

Recall
Among all actual spam messages, how many were successfully detected?

F1-Score
A combined measure based on precision and recall.

Confusion Matrix
The project visualizes:

True Positive (TP): Spam correctly identified as spam

True Negative (TN): Ham correctly identified as ham

False Positive (FP): Ham incorrectly classified as spam

False Negative (FN): Spam incorrectly classified as ham

🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
TF-IDF
Bag of Words
Multinomial Naive Bayes
Logistic Regression

📦 Installation
Clone the repository:

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
Install the required Python libraries:

pip install pandas numpy matplotlib seaborn scikit-learn
▶️ How to Run
Run the Python file:

python copy_of_class_1_ml_pipeline_text.py
If you are using Google Colab, you can also open the original notebook and execute the cells step by step.

🧪 Test Your Own Messages
The project includes a function for testing custom messages:

my_messages = [
    "Hey bro, are we still meeting for pizza tonight at 8?",
    "CONGRATULATIONS! You have won a $1000 Walmart Gift Card. Click here to claim your prize now!",
    "Urgent! Please call customer service immediately regarding your recent bank transaction."
]

test_my_messages(my_messages)
The model returns:

Predicted class

Spam/Ham label
Model confidence
You can modify the messages and experiment with different types of text.

📂 Project Structure
.
├── copy_of_class_1_ml_pipeline_text.py
└── README.md
🔄 Complete Workflow
Raw Data
   │
   ▼
Data Cleaning
   │
   ▼
Feature / Target Separation
   │
   ▼
Train-Test Split
   │
   ▼
Text Feature Engineering
   │
   ├── Bag of Words
   │
   └── TF-IDF
   │
   ▼
Model Training
   │
   ├── Multinomial Naive Bayes
   └── Logistic Regression
   │
   ▼
Prediction
   │
   ▼
Evaluation
   │
   ├── Accuracy
   ├── Precision
   ├── Recall
   ├── F1-Score
   └── Confusion Matrix
🎯 Learning Outcomes
After completing this project, you should understand how to:

Prepare data for machine learning.

Handle basic missing values.
Split data into training and testing sets.
Convert text into numerical features.
Understand Bag of Words and TF-IDF.
Build a text classification model.
Detect spam SMS messages.
Evaluate classification models using multiple metrics.
Compare different machine learning algorithms.
Experiment with your own text inputs.

💡 Key Takeaway
A machine learning project is not just about choosing a model.
A typical workflow is:
Data → Preprocessing → Feature Engineering → Model Training → Prediction → Evaluation
This project provides a practical example of that complete workflow using text classification.

🚀 Future Improvements
Possible extensions include:
Add more text preprocessing techniques.
Compare additional classification algorithms.
Perform hyperparameter tuning.
Add cross-validation.
Build a web interface for real-time spam detection.
Save and load the trained model.
Deploy the classifier as an API or web application.
Test the model on a larger and more diverse SMS dataset.

📚 Reference
The project uses the SMS dataset available through the PyCon 2016 tutorial repository:
https://raw.githubusercontent.com/justmarkham/pycon-2016-tutorial/master/data/sms.tsv


👨‍💻 Author
Sarthak Dewangan
Built as a hands-on Machine Learning and NLP learning project.
⭐ If you found this project useful, consider giving the repository a star!

