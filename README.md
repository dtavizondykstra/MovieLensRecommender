# Movie Recommender System with Cosine Similarity

This project implements a movie recommender system using the [MovieLens](https://grouplens.org/datasets/movielens/) dataset. It focuses on content-based filtering, analyzing movie genres and tags to suggest similar movies to users. 

Here's an overview of the process:

**1. Data Preparation**

* Loads the MovieLens datasets (movies, ratings, tags, links).
* Merges datasets to create a unified DataFrame for analysis.
* Prepares the data for recommendations:
    * Aggregates tags for each movie, creating a comprehensive feature.
    * Calculates the average rating per movie for popularity consideration.
    * Combines genres and tags into a single "combined_features" column for feature engineering.

**2. Building the Recommender System**

* Utilizes CountVectorizer to translate movie descriptions (genres and tags) into numerical features. This allows us to compare movies quantitatively.
* Calculates cosine similarity between movies based on their feature vectors. Cosine similarity measures the angle between these vectors in a multi-dimensional space, where each dimension represents a genre or tag. Movies with similar descriptions have a smaller angle and a higher cosine similarity score (closer to 1).
* Creates a function to recommend movies using cosine similarity scores. This function takes a movie title as input and retrieves the top 10 most similar movies based on their cosine similarity scores.

**3. Testing and Results**

* Tests the recommendation function with a user-selected movie title.
* Verifies the system generates relevant recommendations based on the chosen movie's genres and tags.

This recommender system provides a basic framework for suggesting movies based on content similarity. It can be further enhanced by incorporating collaborative filtering techniques or hybrid approaches to improve the accuracy and personalization of recommendations.


**Additional Information:**

* You can find the code for this project in the Jupyter Notebook file `Tavizon630Week10.ipynb`.
* This project utilizes libraries like Pandas, scikit-learn (CountVectorizer, cosine_similarity), and data_table (for better DataFrame visualization in Google Colab).

**Feel free to explore the code and experiment with different functionalities!**

