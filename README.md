# Netflix_Movie_Recommendation_System

# Content-Based Movie Recommendation System 🎬

This project builds a content-based movie recommendation engine that suggests similar movies based on metadata such as genres, cast, crew, and keywords using NLP techniques.

## 📦 Dataset
- **Source**: [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- **Movies**: ~5,000
- **Files Used**: `movies.csv`, `credits.csv`
- **Merged Features**: Overview, Genres, Keywords, Cast, Crew

## ⚙️ Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn (CountVectorizer, cosine_similarity)
- NLP
- ast (for JSON parsing)

## 🔍 Steps Performed
1. **Data Cleaning & Merging**: Combined `movies` and `credits` on title field.
2. **Feature Engineering**:
   - Normalized text fields (e.g., names like `James Cameron` → `JamesCameron`)
   - Combined metadata into a unified `tags` column
3. **Text Vectorization**: Applied `CountVectorizer` on `tags`
4. **Similarity Matrix**: Computed cosine similarity between all movies
5. **Recommendation Function**: Returns top 5 similar movies to the input title

## 📈 Sample Output
Input: Avatar
→ Recommendations:

John Carter
Guardians of the Galaxy
Aliens
Star Wars: Clone Wars
Star Trek



## 🚀 How to Run
1. Clone this repo
2. Install dependencies:


3. Open and run `Movie_recommendation.ipynb`
4. Call `recommend('Your Favorite Movie')` in a cell

## 📌 Future Enhancements
- Use TF-IDF instead of CountVectorizer for better scoring
- Add rating-based filtering (hybrid model)
- Build a Streamlit/Flask web app interface

## 📁 Project Structure
├── Movie_recommendation.ipynb
├── movies.csv
├── credits.csv
└── README.md
