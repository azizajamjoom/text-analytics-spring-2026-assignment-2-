# Sentiment Analysis on IMDB Reviews

## Project Overview
This project builds a machine learning pipeline to classify movie reviews as **positive** or **negative** using natural language processing (NLP) techniques.

The goal is to evaluate different models and feature engineering methods, compare their performance, and test how well the best model generalizes to new, unseen data.

---

## Dataset
- **Dataset:** IMDB Movie Reviews
- **Size:** 50,000 reviews
- **Classes:** Balanced (positive / negative)

The dataset used for this project is included in this repository:

 `IMDB Dataset.csv`

---

## Project Steps

### Step 1: Obtain Data
- Loaded IMDB dataset into the environment

### Step 2: Exploratory Data Analysis (EDA)
- Checked class distribution
- Analyzed review length
- Visualized distributions

### Step 3: Text Cleaning
- Removed HTML tags
- Removed extra spaces
- Standardized text formatting

### Step 4: Tokenization & Feature Engineering
- Used:
  - **CountVectorizer**
  - **TF-IDF Vectorizer**
- Included unigrams and bigrams
- Limited to top 5,000 features

---

### Step 5: Train Models
Models trained:
- Logistic Regression + Count
- Logistic Regression + TF-IDF
- Naive Bayes + Count
- Naive Bayes + TF-IDF

Additional steps:
- Stratified train-test split (80/20)
- Hyperparameter tuning using GridSearchCV
- Model performance evaluation

---

### Step 6: Evaluate & Compare

Evaluation methods:
- Classification reports
- Confusion matrices
- Model comparison table

**Best Model: Logistic Regression + TF-IDF**
- Accuracy: **0.8951**
- F1 Score: **0.8956**

---

### Step 7: Custom Inference

- Created 20 new examples:
  - 10 easy
  - 5 tricky (mixed sentiment, ambiguity)
  - 5 out-of-domain (TV, podcasts, etc.)

- Ran inference using the best model

Results:
- Correct predictions: **17 / 20**
- Accuracy: **0.85**

Insight:
- Strong performance on clear sentiment
- Struggles with mixed or ambiguous language
- Reasonable generalization to new domains

---

## Key Takeaways
- TF-IDF outperformed CountVectorizer
- Logistic Regression outperformed Naive Bayes
- Model handles clear sentiment well but struggles with nuance
- Generalization is good but not perfect

---

## How to Run This Project

### Option 1: Google Colab (Recommended)
1. Upload the notebook to **Google Colab**
2. Upload the dataset file:
   - `IMDB Dataset.csv`
3. Run all cells step-by-step

**Important:**  
This project is designed to run in **Google Colab**, so make sure to upload both:
- The notebook file
- The dataset file

---

### Option 2: Local Environment
Requirements:
- Python 3.x
- pandas
- numpy
- scikit
