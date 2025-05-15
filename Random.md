import pandas as pd

# Sample movie dataset
movies = pd.DataFrame({
    'movie_id': [1, 2, 3, 4, 5],
    'title': ['Inception', 'Titanic', 'The Matrix', 'Interstellar', 'The Notebook'],
    'genre': ['Sci-Fi', 'Romance', 'Sci-Fi', 'Sci-Fi', 'Romance']
})

# Sample user preferences
user_favorite_genre = 'Sci-Fi'

# Simple recommendation logic
recommended_movies = movies[movies['genre'] == user_favorite_genre]

# Display recommendations
print(f"\nRecommended {user_favorite_genre} movies for you:")
for idx, row in recommended_movies.iterrows():
    print(f"- {row['title']}")
