# Sentiment Analysis Using Transformers and LSTM

This project applies sentiment analysis techniques on textual data using both Transformer-based models (e.g., DistilBERT) and traditional LSTM networks. The goal is to classify text into sentiment categories such as **positive**, **neutral**, and **negative**.

---

## 📚 Project Structure

- `Sentiment_Analysis.ipynb`: Main Jupyter Notebook containing:
  - Data loading and preprocessing
  - Tokenization and vectorization
  - Model training with DistilBERT
  - Comparison with LSTM-based architecture
  - Evaluation and performance metrics

---

## 🔍 Features

- Preprocessing of textual data with Hugging Face Tokenizers
- Fine-tuning of pre-trained DistilBERT model
- LSTM model for baseline comparison
- Accuracy, classification report, and confidence score evaluation
- Visualizations of prediction confidence and distribution

---

## 📦 Dependencies

Make sure to install the required libraries:

```bash
pip install transformers datasets scikit-learn matplotlib seaborn torch lime

