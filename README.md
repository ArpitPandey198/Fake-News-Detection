
# 📰 Fake News Detection using Machine Learning

## 📌 Project Overview

Fake news is misleading or false information presented as news. With the rapid growth of social media and online platforms, identifying potentially unreliable news has become an important challenge.

This project presents a Machine Learning based Fake News Detection system that analyzes news text and predicts whether the given news is **LIKELY REAL** or **LIKELY FAKE**.

The project uses Natural Language Processing (NLP), TF-IDF feature extraction, and Logistic Regression to classify news articles.

The trained machine learning model is integrated with a Flask web application so that users can enter news text through a simple web interface and receive a prediction.

> **Note:** This application is an educational screening tool. Its prediction should not be treated as independent proof that a news story is true or false.

---

## 🎯 Objectives

The main objectives of this project are:

- To detect potentially fake news using Machine Learning.
- To preprocess and clean news text.
- To convert text into numerical features using TF-IDF.
- To train a Logistic Regression classification model.
- To build a simple web application using Flask.
- To display the predicted result and confidence score.
- To evaluate the machine learning model using standard evaluation metrics.

---

## 🚀 Features

- 📰 News headline/article input
- 🧹 Automatic text preprocessing
- 🔤 TF-IDF feature extraction
- 🤖 Logistic Regression classification
- 📊 Prediction confidence score
- 🌐 Flask-based web application
- 📈 Accuracy, Precision, Recall and F1-score evaluation
- 🔢 Confusion Matrix evaluation
- 💻 Simple and user-friendly interface

---

## 🧠 Machine Learning Workflow

The project follows the following workflow:

```text
News Text
    ↓
Text Preprocessing
    ↓
TF-IDF Feature Extraction
    ↓
Logistic Regression Model
    ↓
Prediction
    ↓
LIKELY FAKE / LIKELY REAL
    ↓
Confidence Score
🛠️ Technologies Used
Programming Language
Python
Machine Learning
Scikit-learn
TF-IDF Vectorizer
Logistic Regression
Data Processing
Pandas
Regular Expressions (re)
Web Development
Flask
HTML
CSS
JavaScript
Dataset
CSV-based demonstration dataset
📂 Project Structure
Fake_News_Detection_IBM_Final/
│
├── app.py
├── requirements.txt
├── README.md
│
├── data/
│   └── news.csv
│
├── templates/
│   └── index.html
│
├── static/
│   ├── app.js
│   └── style.css
│
├── evaluation_metrics.json
├── evaluation_report.txt
├── project_report.txt
└── Fake_News_Detection_IBM_PPT.pptx
📄 File Description
app.py
The main Python Flask application.
It:
Loads the news dataset.
Cleans the news text.
Creates the TF-IDF and Logistic Regression pipeline.
Trains the machine learning model.
Provides the prediction endpoint.
Returns the prediction and confidence score.
data/news.csv
Contains the demonstration news dataset.
The dataset includes:
News title
News text
News label (FAKE or REAL)
templates/index.html
Contains the main structure of the web application and user interface.
static/style.css
Contains the styling and visual design of the web application.
static/app.js
Handles:
User input
Sending news text to Flask
Receiving the prediction
Displaying the prediction and confidence score
evaluation_metrics.json
Contains the recorded model evaluation metrics.
evaluation_report.txt
Contains the classification report and evaluation information.
project_report.txt
Contains project methodology, objectives, limitations and future scope.
Fake_News_Detection_IBM_PPT.pptx
Contains the presentation of the project.
📊 Dataset
The project includes a demonstration dataset stored in:
data/news.csv
The current dataset contains:
57 news records
30 REAL records
27 FAKE records
The dataset is included with the project so that the application can run without requiring an external dataset.
This is a small demonstration dataset and should not be considered a large real-world benchmark dataset.
🤖 Machine Learning Model
The project uses a Scikit-learn Pipeline containing two main components:
1. TF-IDF Vectorizer
TF-IDF stands for Term Frequency-Inverse Document Frequency.
It converts text into numerical features that can be processed by a machine learning algorithm.
The project uses:
TfidfVectorizer
with English stop-word removal and unigram/bigram features.
2. Logistic Regression
The extracted TF-IDF features are passed to:
LogisticRegression
The model performs binary classification between:
FAKE
REAL
🧹 Text Preprocessing
Before the news is passed to the machine learning model, the text is cleaned.
The preprocessing includes:
Converting text to lowercase
Removing URLs
Removing unwanted characters
Removing extra spaces
Combining the news title and article text during training
Example:
Original:
"BREAKING! Visit www.example.com for the Latest News!!!"

        ↓

Cleaned:
"breaking visit for the latest news"
📈 Model Evaluation
The project evaluates the machine learning model using standard classification metrics.
The evaluation includes:
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
The recorded evaluation results on the demonstration test set are:
Metric
Score
Accuracy
100%
Precision
100%
Recall
100%
F1-Score
100%
Test Set:
15 records
Confusion Matrix:
              Predicted
              FAKE  REAL

Actual FAKE     7     0
Actual REAL     0     8
⚠️ Evaluation Disclaimer
The above scores are calculated on the included small demonstration dataset.
They should not be interpreted as real-world fake-news detection accuracy.
A larger, diverse and independently verified dataset would be required for meaningful real-world evaluation.
💻 Installation
Step 1: Clone the Repository
git clone YOUR_GITHUB_REPOSITORY_URL
Move into the project folder:
cd Fake_News_Detection_IBM_Final
Step 2: Install Dependencies
Run:
pip install -r requirements.txt
The project uses:
Flask
pandas
scikit-learn
▶️ Run the Application
Start the Flask application using:
python app.py
After the Flask development server starts, open a web browser and visit:
http://127.0.0.1:5000
🖥️ How to Use
Open the web application.
Enter a news headline or article.
Click the Check News button.
The application processes the entered text.
The machine learning model generates a prediction.
The result is displayed as:
LIKELY FAKE
or LIKELY REAL
The model confidence score is also displayed.
🌐 Web Application Architecture
The application works through the following architecture:
User
  ↓
HTML Interface
  ↓
JavaScript
  ↓
Flask /predict Endpoint
  ↓
Text Preprocessing
  ↓
TF-IDF Vectorization
  ↓
Logistic Regression
  ↓
Prediction + Confidence
  ↓
Web Interface
🔐 API Information
This project does not require OpenAI, ChatGPT, Gemini or OpenRouter API keys.
The machine learning model runs locally using Python and Scikit-learn.
Therefore:
No OpenAI API key is required.
No Gemini API key is required.
No OpenRouter API key is required.
No .env file is required for the current implementation.
⚠️ Limitations
The current prototype has some limitations:
The dataset is small.
The dataset is designed for demonstration purposes.
Machine learning predictions are not independent proof of truth.
The model may perform differently on unseen real-world news.
The current system primarily works with English text.
The system does not independently verify news sources or factual claims.
🔮 Future Scope
The project can be improved in the future by:
Using a much larger verified dataset.
Adding multilingual fake-news detection.
Using advanced NLP techniques.
Exploring transformer-based models.
Adding source credibility analysis.
Adding Explainable AI features.
Connecting the system with trusted fact-checking sources.
Improving real-world evaluation using independent datasets.
Adding user authentication and history.
Deploying the application online.
📚 Learning Outcomes
Through this project, the following concepts were implemented:
Python Programming
Data Preprocessing
Natural Language Processing
TF-IDF
Supervised Machine Learning
Logistic Regression
Model Evaluation
Flask Web Development
HTML
CSS
JavaScript
Machine Learning Deployment Concepts
🌍 Applications
A system like this can be used as a preliminary screening tool for:
Online news platforms
Educational projects
Social media monitoring
Research and experimentation
Digital literacy applications
Information verification workflows
However, important information should always be verified using reliable independent sources.
👨‍💻 Project Information
Project Title: Fake News Detection using Machine Learning
Program: IBM / PBEL 3.0 AI & Machine Learning Project
Developer: Arpit Pandey
Technology Stack: Python, Flask, Pandas, Scikit-learn, HTML, CSS and JavaScript
⚖️ Disclaimer
This project is an educational machine-learning prototype.
The prediction provided by the application should be considered a preliminary screening result and not a definitive determination of whether a news story is factually true or false.
Users should verify important information through reliable and independent sources.
📜 License
This project is created for educational and project demonstration purposes.

