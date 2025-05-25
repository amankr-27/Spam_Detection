# 📧 Spam Detection using Machine Learning
This project focuses on developing a machine learning model to classify SMS messages as spam or ham (not spam).The project uses natural language processing (NLP) and a Multinomial Naive Bayes classifier to achieve high accuracy and recall.

# 🧠 Motivation
With the widespread use of messaging and email platforms, spam messages can pose security risks and degrade user experience. Traditional spam filters rely on rule-based systems, which fail to adapt to evolving spam tactics. This project introduces a data-driven approach using machine learning to automatically detect spam with high reliability.

# 🔄 Workflow Overview
# 1. 📥 Data Loading & Inspection
Dataset: spam.csv containing labeled messages.

Columns v1 and v2 renamed to Category (spam/ham) and Message.

# 2. 🧹 Data Preprocessing
Dropped unnecessary columns.

Checked for nulls and duplicates.

Created a binary target column (Spam) with 1 = spam and 0 = ham.

# 3. 📊 Exploratory Data Analysis
Visualized the distribution of spam vs ham.

Used WordCloud to extract frequently used terms in spam messages.

# 4. 🔡 Text Vectorization
Used TF-IDF Vectorizer to convert message text into numerical features.

This transformation helps the model understand word importance in messages.

# 5. 🤖 Model Building
Implemented Multinomial Naive Bayes, known for its efficiency in text classification.

Split the dataset into training and test sets (typically 80/20).

# 6. 📈 Model Evaluation
Primary metric: Recall — chosen to minimize false negatives (i.e., missing a spam message).

Also tracked: Accuracy, Confusion Matrix, and F1 Score.

Achieved 98.49% recall on the test set.


# 🔮 Key Insights
Words like “free”, “call”, “win”, “now” appear frequently in spam.
![Image](Images/Spam message.PNG)


Class imbalance is evident: ~13% spam vs 87% ham.

The classifier performs well even with this imbalance.

# 💡 Future Improvements
Add more classifiers: SVM, Random Forest, Logistic Regression.

Perform hyperparameter tuning using GridSearchCV.

Use cross-validation to avoid overfitting.

Deploy the model via Flask or Streamlit for real-time spam detection.
