# 📊 Yelp Review Sentiment Analysis with LSTM & DistilBERT


## 📌 Overview
This project implements and compares two deep learning approaches for sentiment classification on Yelp restaurant reviews:

- **Bidirectional LSTM** — A custom recurrent neural network
- **DistilBERT** — A distilled version of BERT optimized for speed and efficiency

The goal is to classify reviews into three sentiment categories:
- 😠 **Bad** (1–2 stars)
- 😐 **Neutral** (3 stars)
- 😃 **Good** (4–5 stars)

Key features include class imbalance handling, model interpretability with LIME, and a detailed performance comparison.

---

## ✨ Key Features
- ✅ Dual-model architecture for performance benchmarking  
- ⚖️ Class weighting for imbalanced sentiment distribution  
- 🔍 LIME interpretability to explain model predictions  
- 📏 Review length-based performance analysis  
- 📊 Confidence metrics for prediction reliability  
- 📈 Comprehensive training and evaluation visualizations  

---

## 📊 Dataset
The system uses the **Yelp Restaurant Reviews** dataset containing:

- 19,000+ reviews with star ratings (1–5)
- Cleaned & preprocessed text (punctuation/symbols removed)

**Class distribution after preprocessing:**

| Sentiment | Percentage | Count   |
|-----------|------------|---------|
| Good      | 77.1%      | 15,330  |
| Neutral   | 10.4%      | 2,069   |
| Bad       | 12.6%      | 2,497   |

---

## 📈 Results
**🔁 Performance Comparison**

| Model	     | Accuracy | F1-Score	| Training Time |	Memory Usage |
|------------|----------|-----------|---------------|--------------|
| LSTM       | 78%	    | 80%     	| Fast        	| Low          |
| DistilBERT | 87%      |	87%	      | Slow	        | High         |


**🎯 Per-Class Accuracy**

| Sentiment |	LSTM  | DistilBERT |
|-----------|-------|------------|
| Bad	      | 76.8% |	71.7%      |
| Neutral   |	32.6%	| 46.9%      |
| Good	    | 84.6%	| 94.8%      |

**📏 Review Length Analysis**

| Review Length   	| LSTM  | DistilBERT |
|-------------------|-------|------------|
| Short (≤20 words) | 90.4% |	93.5%      |
| Long (>20 words)  |	77.4%	| 86.5%      |

**🔍 Model Interpretability**

LIME (Local Interpretable Model-agnostic Explanations) helps visualize which words influenced the prediction.

➡️ [View LIME Explanation for LSTM Model](visualizations/lstm_explanation.html)

➡️ [View LIME Explanation for DistilBERT Model](visualizations/bert_explanation.html)

> Example Review: *"I had to wait forever for my order. The service was painfully slow and completely unacceptable."*
---
