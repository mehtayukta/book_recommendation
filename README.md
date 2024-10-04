# Wide and Deep Learning-Based Recommender System for Book Reviews

This repository contains the implementation of a **Wide and Deep Learning-based recommender system**, inspired by the paper [Wide & Deep Learning for Recommender Systems](https://arxiv.org/abs/1606.07792). The model is built for the Book Review dataset, which contains user ratings for various books, aiming to learn both shallow (wide) and deep patterns in the data for more accurate recommendations.
Recommender systems aim to predict a user's rating for an item, and Wide & Deep models combine the strength of two approaches:
- **Wide model**: Memorizes feature interactions.
- **Deep model**: Generalizes to unseen feature combinations.

This project implements a Wide and Deep Recommender System based on TensorFlow/Keras, and evaluates its accuracy using an 80/20 train-test split.

## Dataset

The dataset used for this project is sourced from [Kaggle Book Recommendation Dataset](https://www.kaggle.com/code/jirakst/book-recommendation/input). It contains user reviews, ratings, and item information for books.

## Model Architecture

The **Wide and Deep Model** architecture combines:
- **Wide Part**: Uses sparse features (e.g., user/book ID) to capture feature interactions.
- **Deep Part**: Uses dense features (e.g., user/book embeddings) to capture nonlinearities in the data.

### Input Features:
1. **User Features**: User ID, preferences, embeddings.
2. **Item Features**: Book ID, book features like genre, author, etc.

### Wide & Deep Layers:
- **Wide Model**: Linear model for memorization of co-occurrence patterns.
- **Deep Model**: A neural network for generalization with multiple layers of dense, ReLU-activated units.

### Output:
The final output is the predicted rating for a user-book pair.


