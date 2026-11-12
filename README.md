# 🎬 Movie Recommendation System

A content-based movie recommender that suggests similar movies based on a movie you choose. It uses **TF-IDF** on movie metadata and cosine similarity, with a **FastAPI** backend and a **Streamlit** frontend. Movie details and posters are fetched from the **TMDB API**.


## ✨ Features

- Search for a movie and get a list of similar recommendations
- Content-based filtering using TF-IDF and cosine similarity
- FastAPI backend serving recommendations
- Streamlit interface for easy use
- Movie details/posters from the TMDB API

## 🧠 How It Works

1. Movie metadata is cleaned and combined into text
2. TF-IDF converts that text into numerical vectors
3. Cosine similarity finds the movies closest to the selected one
4. The top matches are returned as recommendations

The trained TF-IDF model and matrices are saved with `joblib` (`tfidf.joblib`, `tfidf_matrix.joblib`, `df.joblib`, `indices.joblib`), so the app loads fast without retraining.

## 📁 Project Structure

- `movies.ipynb`: data cleaning, TF-IDF and model building
- `main.py`: FastAPI
