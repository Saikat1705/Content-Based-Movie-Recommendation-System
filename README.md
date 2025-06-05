# 🎬 Content-Based Movie Recommendation System

This project is a Python-based content-based movie recommendation system using the **TMDB 5000 Movie Dataset**. It suggests similar movies based on genres, keywords, cast, crew, and plot overview using **NLP techniques** and **cosine similarity**.

---

## 🔍 Features

- Recommends movies similar to the one you input
- Uses movie metadata: genres, cast, crew, keywords, and overview
- NLP-based preprocessing
- Cosine similarity for recommendation
- Built using `pandas`, `scikit-learn`, and `CountVectorizer`

---

## 📁 Dataset

- [`tmdb_5000_movies.csv`](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- [`tmdb_5000_credits.csv`](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

> Download the dataset from Kaggle and place both files in the same directory as the script.

---

## 🚀 How It Works

1. Loads and merges movie metadata with credits
2. Extracts useful fields: genres, cast, crew, keywords
3. Preprocesses text (lowercase, removing spaces, etc.)
4. Creates a “tag” column combining all features
5. Vectorizes text using `CountVectorizer`
6. Calculates cosine similarity between all movies
7. Recommends top 5 similar movies

---

## 🧪 Example

```python
>>> recommend('Avatar')
['Titan A.E.', 'Small Soldiers', 'Independence Day', "Ender's Game", 'Aliens vs Predator: Requiem']
