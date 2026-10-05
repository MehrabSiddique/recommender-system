#  Movie Recommender System

A **content-based movie recommendation system** built with Python and NLP techniques. The system recommends movies based on similarities in their plot descriptions, genres, keywords, cast, and directors.

##  Overview

This project uses the TMDB 5000 Movies and Credits datasets to build a content-based recommendation engine.

Instead of relying on user ratings, the system analyzes the characteristics of each movie and recommends movies with similar content.

##  Workflow

```text
TMDB Movies + Credits
        ↓
Data Cleaning & Merging
        ↓
Extract Genres, Keywords, Cast & Director
        ↓
Combine Movie Metadata
        ↓
Create Movie Tags
        ↓
Text Preprocessing
        ↓
Porter Stemming
        ↓
CountVectorizer
        ↓
Cosine Similarity
        ↓
Top 5 Movie Recommendations
```

##  Methodology

### 1. Data Loading

The project uses Pandas to load the TMDB movies and credits datasets.

### 2. Data Integration

The two datasets are merged using the movie title.

### 3. Feature Extraction

The following information is extracted:

* Movie overview
* Genres
* Keywords
* Top cast members
* Director

### 4. Feature Engineering

These features are combined into a single `tags` field representing the content of each movie.

### 5. Text Preprocessing

The project performs:

* Lowercase conversion
* Stop-word removal during vectorization
* Porter stemming using NLTK

### 6. Text Vectorization

`CountVectorizer` converts movie tags into numerical feature vectors using up to 5,000 features.

### 7. Similarity Calculation

Cosine similarity is calculated between movie vectors to measure content similarity.

### 8. Recommendation

Given a movie title, the system identifies the most similar movies and returns the top five recommendations.

##  Technologies

* Python
* NumPy
* Pandas
* Scikit-learn
* NLTK
* CountVectorizer
* Cosine Similarity

##  Dataset

TMDB 5000 Movies and Credits dataset.

##  Example

```python
recommend('Avatar')
```

The system returns five movies with the highest content similarity to the selected movie.

##  Learning Outcomes

* Text preprocessing
* Feature engineering
* NLP fundamentals
* Vectorization
* Similarity-based recommendation
* Data cleaning and integration


##  Notebook

The complete implementation is available in `movies_recommender.ipynb`.
