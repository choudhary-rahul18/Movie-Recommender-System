# Movie-Recommender-System

This is a content-based Movie Recommender System built using **Python**, **Pandas**, and **scikit-learn**. The model suggests movies similar to a user's favorite by analyzing movie descriptions, genres, cast, crew, and keywords from the **TMDB 5000 Movie Dataset**.

## Files in the Repository

| File | Description |
|------|-------------|
| `Movie Recommender.ipynb` | Jupyter Notebook containing all code steps |
| `tmdb_5000_movies.csv` | Movie metadata from TMDB |
| `tmdb_5000_credits.csv` | Cast and crew data |
| `movies.pkl` | Pickle file of the cleaned and processed movie dataset |
| `similarity.pkl` | Pickle file of the cosine similarity matrix |
| `movies_dict.pkl` | Dictionary version of the movie dataset for easy lookup |

## Features Used for Recommendation
- **Overview (Plot)**  
- **Genres**  
- **Top 3 Cast Members**  
- **Director**  
- **Keywords**

All features are combined and processed to create a **"tag"** for each movie. The tags are stemmed and vectorized using **CountVectorizer** and compared using **Cosine Similarity**.

## Technologies & Libraries Used
- Python 3
- Pandas, NumPy
- NLTK (for stemming)
- Scikit-learn (for vectorization and similarity)
- Pickle (for model export)

## How It Works
1. Data from movies and credits CSVs are merged on the movie title.
2. Text features are extracted and cleaned.
3. Tags are created by combining overview, genres, cast, crew, and keywords.
4. Tags are vectorized using **CountVectorizer (max_features=5000)**.
5. Cosine Similarity is computed to measure movie-to-movie closeness.
6. The top 5 most similar movies are recommended when a user inputs a movie name.

### Sample Usage
```python
recommend('Batman')
