# Movie Recommendation Engine

A **Content-Based Movie Recommendation System** built using **Python**, **Natural Language Processing (NLP)**, and **Streamlit**. The application recommends movies similar to a user's selected movie by analyzing movie metadata such as genres, keywords, cast, crew, and overview.

The recommendation engine uses **text vectorization** and **cosine similarity** to identify movies with similar content and presents recommendations through an interactive Streamlit web interface.

---

## Features

- Content-based movie recommendations
- NLP-based feature extraction from movie metadata
- Cosine similarity for similarity matching
- Interactive Streamlit web application
- Fast recommendation generation using precomputed similarity matrices

---

## How It Works

The recommendation pipeline consists of the following steps:

1. Dataset loading
2. Data cleaning and preprocessing
3. Feature engineering by combining relevant movie attributes
4. Text vectorization
5. Cosine similarity computation
6. Recommendation generation
7. Streamlit web interface

---

## Recommendation Approach

This project uses **Content-Based Filtering**.

Instead of recommending movies based on other users' preferences, it recommends movies that are similar to the selected movie by comparing their features.

### Why Content-Based Filtering?

- Recommends movies with similar content
- Does not require user ratings
- Reduces the cold-start problem
- Easy to understand and implement

---

## Dataset

This project uses the **TMDB 5000 Movie Dataset**.

Dataset: https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata

The repository includes:

- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Streamlit
- Pickle

---

## Project Structure

```text
Movie-Recommendation-Engine/
│
├── Datasets/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
│
├── get_recommendation.ipynb
├── app.py
├── similarity.pkl
├── movie_list.pkl
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone <repository-url>
cd Movie-Recommendation-Engine
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Or install them individually:

```bash
pip install pandas numpy scikit-learn nltk streamlit
```

---

## Running the Project

### Step 1: Generate Recommendation Files

Open and run:

```text
get_recommendation.ipynb
```

This notebook processes the dataset and generates:

- `movie_list.pkl`
- `similarity.pkl`

### Step 2: Launch the Streamlit App

```bash
streamlit run app.py
```

The application will launch locally in your browser.

---

## Recommendation Method

The recommendation engine follows these steps:

- Combine important movie features into a single text representation.
- Clean and preprocess the text.
- Convert the text into numerical vectors using text vectorization.
- Compute cosine similarity between movie vectors.
- Sort similarity scores to recommend the most similar movies.

---

## Future Improvements

- TMDB API integration for movie posters and additional details
- Hybrid recommendation system
- Personalized recommendations based on user history
- Genre and language filters
- Deployment on Streamlit Cloud

---

## License

This project is intended for educational and learning purposes.
