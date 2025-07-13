# Movie Recommendation Engine with PySpark

This project implements a movie recommendation system using collaborative and content-based filtering techniques on the MovieLens dataset. The primary goal is to predict user movie preferences and provide personalized recommendations. The project leverages PySpark for scalable data processing and model building.

## Project Overview

This recommendation system addresses the challenge of information overload by helping users discover movies they are likely to enjoy. It uses two main approaches:

1.  **Collaborative Filtering (CF):** This method recommends movies based on the preferences of similar users. It operates on the principle that if two users have rated several movies similarly, they are likely to have similar tastes in other movies as well. This project uses the Alternating Least Squares (ALS) algorithm for collaborative filtering.

2.  **Content-Based Filtering (CBF):** To address the "cold start" problem inherent in collaborative filtering (where it's difficult to make recommendations for new users with little to no rating history), a content-based filtering system is also implemented. This system recommends movies based on their attributes, such as genre, release year, and user-assigned tags.

## Key Features

*   **Personalized Recommendations:** Generates movie recommendations tailored to individual user tastes.
*   **Scalable Implementation:** Built with PySpark to handle large datasets efficiently.
*   **Hybrid Approach:** Combines collaborative and content-based filtering to provide robust recommendations and mitigate the cold-start problem.
*   **Model Evaluation:** The collaborative filtering model's performance is evaluated using Root Mean Squared Error (RMSE) and Precision@10.

## Dataset

This project uses the **MovieLens (ml-latest-small)** dataset, which includes:
*   **ratings.csv:** User IDs, movie IDs, and ratings (1-5 stars).
*   **movies.csv:** Movie IDs, titles, and genres.
*   **tags.csv:** User IDs, movie IDs, and user-generated tags.

## Technologies Used

*   **Python**
*   **PySpark**
*   **Pandas**
*   **Jupyter Notebook** (or any other Python environment)

## Results

### Collaborative Filtering Performance

The collaborative filtering model achieved the following results:

*   **Root Mean Squared Error (RMSE):** 0.87
    *   This indicates that, on average, the model's predicted ratings are off by less than one star from the actual user ratings.
*   **Precision@10:** 0.65
    *   This means that, on average, 6.5 out of the top 10 recommended movies were relevant to the user.

### Content-Based Filtering

The content-based filtering system successfully generates recommendations for users with limited interaction history by finding movies with similar attributes (genre, tags, release year) to those they have already liked.
