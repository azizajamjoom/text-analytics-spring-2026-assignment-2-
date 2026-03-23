# Sentiment Analysis on IMDb Reviews  

**Student Name:** Aziza Jamjoom  
**Date:** March 2026  
**Dataset:** IMDb Movie Reviews  

---

## Overview  

This project builds a **binary text classification model** to classify movie reviews as either **positive (1)** or **negative (0)**.  

The goal is to develop a model that can accurately interpret sentiment in text data and generalize to new, unseen examples. This type of model can be applied to real-world use cases such as customer feedback analysis, brand monitoring, and content moderation.

---

## Dataset Details  

- **Source:** IMDb Reviews Dataset  
- **Size:** 50,000 reviews  
- **Classes:**  
  - Positive (1): 25,000  
  - Negative (0): 25,000  
- **Distribution:** Balanced (50/50 split)  

The dataset contains raw text reviews that require preprocessing before being used for machine learning.

---

## Dataset Download 

Due to GitHub file size limitations, the dataset is **not stored directly in this repository**.

 Download the dataset here:  
https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews  

Alternatively, you can find the link inside the `/data` file in this repository.

---

## Setup Instructions (Google Colab)   

Follow these steps before running the notebook:

1. Download the dataset from the link  
2. Extract the dataset file (if zipped)  
3. Open the notebook in **Google Colab**  
4. Upload the dataset file:
   - Click **"Files" → Upload**
   - Select the dataset file (CSV)

5. Ensure the file path in the notebook matches the uploaded file  

6. Run all cells from top to bottom  

 The notebook will not run correctly unless the dataset is uploaded first.

---

## Modeling Approach  

- **Preprocessing:**  
  - Removed HTML tags  
  - Removed extra spaces  

- **Feature Engineering:**  
  - Count Vectorization  
  - TF-IDF Vectorization  

- **Models Tested:**  
  - Logistic Regression  
  - Naive Bayes  

- **Hyperparameter Tuning:**  
  - GridSearchCV used for optimization  

---

## Best Model Results  

**Best Model:** Logistic Regression + TF-IDF  

| Metric        | Value   |
|--------------|--------|
| Accuracy      | 0.895 |
| Precision     | 0.89  |
| Recall        | 0.90  |
| F1 Score      | 0.896 |
| Training Time | Fast (efficient linear model) |

---

## Important Class / Label  

Although the dataset is balanced, **negative sentiment is more critical from a business perspective**.  

Missing negative reviews (missed detections) can hide customer dissatisfaction and delay necessary action. Therefore, recall for the negative class is especially important.

---

## Model Comparison (5 Criteria)  

| Model            | Accuracy | F1 Score | Interpretability | Speed | Generalization |
|------------------|----------|----------|------------------|-------|----------------|
| LR + TF-IDF      | **0.895** | **0.896** | High             | Fast  | Strong         |
| LR + Count       | 0.878    | 0.878    | High             | Fast  | Good           |
| NB + TF-IDF      | 0.860    | 0.863    | Medium           | Very Fast | Moderate     |
| NB + Count       | 0.839    | 0.839    | Medium           | Very Fast | Weak         |

---

## Custom Inference Summary  

- **Correct Predictions:** 17 / 20  
- **Custom Accuracy:** 85%  

### Key Findings:
- Strong performance on **clear sentiment examples**  
- Errors occurred in:
  - **Tricky examples** (mixed sentiment, ambiguity)  
  - **Out-of-domain examples** (e.g., podcasts, documentaries)  

---

## Recommendation  

 **Recommended Model:** Logistic Regression + TF-IDF  

### Justification:
- Highest F1 score and accuracy  
- Balanced performance across both classes  
- Interpretable and efficient  
- Strong generalization to new data  

### Business Impact:
- Enables scalable sentiment monitoring  
- Helps identify customer dissatisfaction early  
- Supports data-driven decision making  

---

## Limitations  

- Struggles with:
  - Mixed sentiment (e.g., “good acting but bad plot”)  
  - Sarcasm and ambiguous language  
- Slight drop in performance on out-of-domain data  

### Future Improvements:
- Use transformer-based models (e.g., BERT)  
- Train on more diverse datasets  
- Implement continuous retraining  

---


---

## Final Note  

This project demonstrates a complete machine learning pipeline for text classification, including preprocessing, feature engineering, model comparison, evaluation, and real-world testing through custom inference.
