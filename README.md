# 📝 Customer Feedback Analysis using Machine Learning

#Overview

This project is a Streamlit-based web application that analyzes customer feedback (Amazon Alexa reviews) and predicts whether the sentiment is **Positive or Negative** using multiple Machine Learning models.

It also provides model evaluation metrics, dynamic confusion matrix, and word cloud visualizations for better insights.

---

#Features

* 🔍 Sentiment Prediction
    * Predicts whether a review is Positive or Negative
    * Supports multiple ML models

* 📊 Model Evaluation
    * Accuracy, Precision, Recall, F1 Score (2×2 layout)
    * Dynamic Confusion Matrix (no static images)

* ☁️ Word Cloud Visualization
    * All reviews
    * Positive reviews
    * Negative reviews

* ⚡Smart Training System
    * Models are trained **only once**
    * Automatically retrains if dataset changes (hash-based detection)

# 🧠 Machine Learning Models Used
  * Random Forest
  * Decision Tree
  * XGBoost
  * Naive Bayes
  * Support Vector Machine (SVM)

#🗂️ Project Structure

```
📁 project-folder
│
├── streamlit_app.py        # Main application file
├── amazon_alexa.tsv        # Dataset
├── models/                 # Saved models (.pkl files)
│   ├── model_rf.pkl
│   ├── model_dt.pkl
│   ├── model_xgb.pkl
│   ├── model_nb.pkl
│   ├── model_svm.pkl
│   ├── vectorizer.pkl
│   └── data_hash.txt
│
└── README.md
```

#⚙️ Installation

1️⃣ Clone the repository

```
git clone <your-repo-link>
cd project-folder
```

2️⃣ Install dependencies
```
pip install -r requirements.txt
```

Or manually install:
```
pip install streamlit pandas scikit-learn matplotlib seaborn xgboost wordcloud
```

▶️ Run the Application
    ```
    streamlit run streamlit_app.py
    ```

🔄 How It Works

✔ Training Logic
  * If models are not present → trains models
  * If dataset changes → retrains automatically
  * Otherwise → uses saved models

✔ Prediction Flow
  1. User inputs review text
  2. Text is cleaned (lowercase, remove symbols)
  3. Converted using TF-IDF
  4. Model predicts sentiment

#📊 Evaluation Metrics
  * Accuracy – Overall correctness
  * Precision – Correct positive predictions
  * Recall – Ability to find all positives
  * F1 Score – Balance between precision & recall

## ⭐ If you like this project
Give it a star ⭐ on GitHub!
