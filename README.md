# Kindle-book-recommendation-system-ml

The objective of this project is to develop a book recommendation system that leverages two key approaches: Collaborative Filtering and Popularity-Based Recommendation. These techniques provide personalized and contextually relevant book suggestions based on user preferences, past behavior, and the overall popularity of books. By combining these two methods, the system aims to provide more diverse and accurate book recommendations to users.

# Dataset and Preprocessing:

The project uses a dataset that includes information about books, user ratings, and book attributes such as Book-Title, Book-Author, Book-Rating, and Image-URL-M. Each user has rated books on a scale from 1 to 5, and these ratings reflect their satisfaction with the books. The data is cleaned and processed to ensure consistency and reliability. The key data points used for recommendations are the Book-Title and Book-Rating columns, which form the basis of our recommendation system.

# Link to Dataset:

https://drive.google.com/drive/folders/1gwJXKGvD7ph4SJ4WbLq3yZmSCVjK71Ex

# Collaborative Filtering Approach:

Collaborative filtering is a popular recommendation technique that relies on the idea that users who have agreed on one topic will also agree on other topics. In this project, we focus on user-item collaborative filtering, where the system recommends books based on the preferences of similar users.

To achieve this, the dataset is converted into a pivot table (pt), where each row represents a user and each column represents a book, with values corresponding to the ratings given by the users. The similarity between books is calculated using cosine similarity, which measures how similar two books are based on user ratings. If two books have similar ratings across multiple users, they are considered similar, and one can be recommended to users who liked the other.

When a user provides a rating for a book, the system identifies the top-N most similar books based on their cosine similarity scores. These similar books are recommended to the user. This recommendation process ensures that books with a high likelihood of being appreciated by the user are suggested, based on the behavior of similar users.

# Popularity-Based Approach:

In addition to collaborative filtering, a popularity-based recommendation approach is also employed. Popularity-based recommendations suggest books based on their overall popularity within the user base, rather than the preferences of individual users. Books that have received the highest average ratings or have been rated by the most users are considered "popular" and are recommended to users as a way to ensure that they discover widely appreciated books.

This approach can be particularly useful in cases where the collaborative filtering model does not have enough user data or when users are new, as it ensures that they are still exposed to well-regarded books within the system. The popularity score can be computed based on the number of ratings a book has received or its average rating, and the most popular books are recommended as an alternative when collaborative filtering may not generate sufficient recommendations.
