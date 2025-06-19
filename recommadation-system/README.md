# 🎬 MovieLens LightGBM Learning-to-Rank Recommender

This project implements a **Learning-to-Rank (LTR)** recommendation system using **LightGBM** on the **MovieLens dataset**. It predicts personalized top-N movie recommendations for users based on movie genres, ratings, and user-item interaction statistics.

---

## 📂 Dataset

- **MovieLens Latest** dataset from [GroupLens](https://grouplens.org/datasets/movielens/)
- Files used:
  - `ratings.csv`: userId, movieId, rating, timestamp
  - `movies.csv`: movieId, title, genres

---

## 🔧 Tools & Technologies

- Python, Pandas, NumPy
- Scikit-learn (train/test split, preprocessing)
- LightGBM (`lambdarank` objective)
- NDCG evaluation

---

## 📈 Project Workflow

### 1. **Data Preprocessing**
- One-hot encode movie genres using `MultiLabelBinarizer`
- Merge ratings and movie metadata
- Engineer features such as user and movie rating statistics

### 2. **Modeling with LightGBM LTR**
- Use `lambdarank` objective to rank items per user
- Group ratings by `userId` for proper LTR training
- Evaluate using global NDCG (Normalized Discounted Cumulative Gain)

### 3. **Generate Recommendations**
- Predict top-N unseen movies for a given user
- Output movie titles sorted by predicted rating

---

## 🧠 Key Learnings

- Implemented a recommender system using learning-to-rank techniques
- Learned how to apply group-based training with LightGBM
- Used NDCG to evaluate ranking quality
- Built a practical, scalable recommendation pipeline

---
