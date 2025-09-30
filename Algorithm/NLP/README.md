# NLP Classification: Sentiment Analysis - Toxicity Detection

This project is a **practical introduction to Natural Language Processing (NLP) and Machine Learning Classification**, focused on building and evaluating models
that distinguish between **toxic** and **non-toxic** social media content.

The task is also highly relevant for:
- Platform moderation  
- Content filtering  
- Maintaining healthy online communities  

---

## Workflow (Data Science Pipeline)

1. **Data Loading & Cleaning**  
   - Import dataset (`twitter.csv`)  
   - Remove noise: mentions, links, hashtags, punctuation  
   - Apply tokenization, stopword removal, lemmatization  

2. **Exploratory Data Analysis (EDA)**  
   - Check class imbalance  
   - Analyze tweet length distributions  
   - Visualize frequent words per class  

3. **Feature Engineering**  
   - Bag-of-Words using `CountVectorizer` (max_features=10,000)  
   - Alternative: `TfidfVectorizer` (commented in code for experimentation)  

4. **Model Training & Evaluation**  
   - Logistic Regression  
   - Multinomial Naive Bayes  
   - Gaussian Naive Bayes  
   - Evaluate with **Accuracy, Precision, Recall, and F1-Score**  

---

## Dataset Overview: `twitter.csv`

| Column   | Description |
|----------|-------------|
| **id**   | Unique identifier for tweet |
| **label**| Target variable: `0 = Non-Toxic`, `1 = Toxic` |
| **tweet**| Raw text content |

**Key Challenge**: Severe class imbalance  
- Non-Toxic (0) : ~29,720 tweets  
- Toxic     (1) : ~2,242 tweets  
- Ratio         : ~13:1  

---

## Exploratory Data Analysis Findings

- **Class Distribution:** Heavy imbalance toward non-toxic tweets.  
- **Tweet Length:** Most tweets are short (5–12 words). Toxic and non-toxic share similar length profiles.  
- **Top Words:**  
  - Non-Toxic: Words like `love`, `day`, `good`.  
  - Toxic: Contains negative/abusive terms.  

---

## Models and Results

| Model                    | Accuracy | F1-Score (Toxic) | Precision (Toxic) | Recall (Toxic) |
|--------------------------|----------|------------------|-------------------|----------------|
| **Multinomial Naive Bayes** | ~0.82   | **0.652**        | 0.678             | 0.629          |
| Logistic Regression       | ~0.86   | 0.639            | **0.843**         | 0.515          |
| Gaussian Naive Bayes      | ~0.70   | 0.323            | 0.215             | **0.647**      |

---

### Best Model: Multinomial Naive Bayes
- **F1-Score = 0.652 (Toxic class)**  
- Best balance between Precision & Recall.  
- Reliable at identifying toxic tweets without excessive false alarms.  

---

## Why Accuracy Alone is Misleading
- Dataset is **93% Non-Toxic**.  
- A model predicting only "Non-Toxic" achieves ~93% Accuracy but **fails completely at detecting Toxic tweets**.  
- Hence, **F1-Score for Label 1 (Toxic)** is the key evaluation metric.  

---

## Prediction on New Input
Example test cases included in the script:
- Positive sentiment → classified as **Non-Toxic (0)** 😊  
- Abusive/negative sentiment → classified as **Toxic (1)** 😠  

---

## Conclusion
- **Multinomial Naive Bayes** currently offers the best trade-off between Precision and Recall.  
- The project highlights the importance of **choosing the right evaluation metric (F1)** in imbalanced datasets.  
- Next steps: Improve generalization with balancing techniques and more advanced models.  

---

## Future Improvements
- Apply **SMOTE** or class-weighting to address imbalance.  
- Explore advanced vectorization: **TF-IDF, n-grams**.  
- Try stronger models: **SVM, Random Forest, or Transformers (BERT, RoBERTa)**.  
- Use **data augmentation** to expand Toxic samples.

---
