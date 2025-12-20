# Movie Recommender System

## Problem Statement
Design and implement a personalized movie recommender system that suggests relevant movies to users based on their historical ratings and similarities with other users. The objective is to enhance user experience by leveraging collaborative filtering techniques and comparing multiple recommendation approaches.

---

## Dataset
The system uses the MovieLens dataset consisting of:
- **ratings.dat**: User–movie ratings with timestamps  
- **users.dat**: User demographic information  
- **movies.dat**: Movie metadata (title and genres)

Ratings are provided on a 5-star scale, and each user has rated at least 20 movies.

---

## Objective
- Generate personalized movie recommendations for users
- Compare the performance of multiple collaborative filtering techniques
- Evaluate strengths and limitations of each approach

---

## Approaches Implemented

### 1. Collaborative Filtering
Leverages collective user behavior to identify preferences.

#### a. User-Based Collaborative Filtering
- Computes similarity between users based on rating patterns
- Recommends movies liked by similar users
- Similarity metrics:
  - **Pearson Correlation**
  - **Cosine Similarity**
- Nearest Neighbors approach for recommendation generation

#### b. Item-Based Collaborative Filtering
- Computes similarity between movies based on user ratings
- Recommends movies similar to those a user has rated highly
- More stable for large user bases
- Similarity metrics:
  - **Pearson Correlation**
  - **Cosine Similarity**

---

### 2. Matrix Factorization
- Decomposes the user–item interaction matrix into latent factors
- Captures hidden relationships between users and movies
- Reduces sparsity and improves scalability
- Learns compact user and movie embeddings

---

### 3. Autoencoder Neural Network
- Treats recommendation as a reconstruction problem
- Learns latent representations of user preferences
- Handles sparse rating matrices effectively
- Improves recommendation quality by modeling non-linear patterns

---

## Evaluation Strategy
- Compare models based on:
  - Prediction accuracy (e.g., RMSE / MAE)
  - Recommendation relevance
- Analyze trade-offs between interpretability, scalability, and performance

---

## Outcome
The project demonstrates how different collaborative filtering techniques perform on the same dataset and highlights the effectiveness of traditional similarity-based methods versus latent factor and neural network–based approaches for personalized movie recommendations.
