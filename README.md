# 🎬 Movie Recommendation System

This project implements multiple recommendation system approaches to predict movie ratings and recommend movies to users. The system uses three CSV files as input:

* **ratings.csv** → User ratings for movies
* **movies.csv** → Movie details (title, genre, etc.)
* **users.csv** → User information

---

## 🚀 Approaches Implemented

### 1. Collaborative Filtering

* **Item-Item Similarity** → Computed similarity between movies based on user ratings.
* **User-User Similarity** → Computed similarity between users based on their rating patterns.
* Built functions:

  * `predict_user_based(user_id, movie_id)` → Predict rating using similar users.
  * `predict_item_based(user_id, movie_id)` → Predict rating using similar movies.

---

### 2. Content-Based Filtering

* Extracted **features from genres** of movies.
* Used **Hamming Distance** to calculate similarity between two movies based on genre overlap.
* Recommended movies similar to what the user has already watched and liked.

---

### 3. Regression-Based Model

* Engineered **user features** and **item features** into a combined dataframe.
* Trained a **GradientBoostingRegressor** to predict ratings.
* This allowed mixing both collaborative and content signals into a predictive ML model.

---

### 4. Matrix Factorization

* Decomposed the user–item rating matrix into **latent factors**.
* Used this to learn hidden patterns (e.g., user preferences & movie traits).
* Generated rating predictions by reconstructing the matrix from latent factors.

---

## 📊 Tech Stack

* **Language**: Python
* **Libraries**: Pandas, NumPy, Scikit-learn, Scipy, Matplotlib/Seaborn (for visualization)

---

## 🏗️ Project Structure

```
├── data/
│   ├── ratings.csv
│   ├── movies.csv
│   └── users.csv
├── notebooks/
│   └── recommendation_system.ipynb
└── README.md
```

---

## 📌 Future Improvements

* Hybrid Recommendation (combining collaborative + content + regression + MF).
* Deploy as a **Flask/Streamlit web app** for interactive recommendations.
* Optimize matrix factorization using **SVD / ALS / Neural Nets**.

