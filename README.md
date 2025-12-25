# Movie Recommendation System

This project implements a comprehensive movie recommendation system using collaborative filtering, matrix factorization, and neural network autoencoders. The system leverages user ratings, movie metadata, and latent factor modeling to provide personalized recommendations and analyze user and movie behavior.

---

## Project Overview

The goal of this project is to build a robust movie recommendation system and extract insights from user behavior and movie characteristics. Key objectives include:

- Understanding user demographics and engagement patterns
- Analyzing movie popularity, ratings, and genre distribution
- Evaluating collaborative filtering methods and their limitations under sparsity
- Implementing latent factor models (Matrix Factorization) and neural network autoencoders
- Generating top-N recommendations and similar movie suggestions

---

## Dataset

- **Users:** 6,040
- **Movies:** 3,883
- **Ratings:** 1,000,209
- **Sparsity:** ~95%
- **Source:** MovieLens-style dataset with user demographics and movie genres

**Columns:**

- `UserID`, `Gender`, `Age`, `Occupation`, `Zip-code`
- `MovieID`, `Title`, `Release_Year`, genre indicators
- `Rating`, `Timestamp`

Each user has at least 20 ratings, minimizing cold-start issues.

---

## Exploratory Data Analysis

Key findings from descriptive and graphical analysis:

- Users are mostly males aged 18–44; college graduates and executives dominate.
- Ratings are positively biased (median ~3.58); engagement peaks on weekends and evenings.
- Movies: Drama, Comedy, and Action dominate; niche genres like Film-Noir and Documentary are highly rated but less popular.
- Temporal trends: Classic movies (1920–1960) have higher average ratings, while 1990s movies dominate in production and total ratings.

---

## Modeling Approaches

1. **Collaborative Filtering (Neighborhood Methods)**
   - Pearson correlation
   - Cosine similarity (user-item)
   - KNN-based cosine
   - Limitations: ineffective under ~95% sparsity; inflated similarity scores; poor personalization

2. **Matrix Factorization (ALS)**
   - Latent factor modeling
   - Metrics: RMSE = 0.8775, MAPE = 0.2626
   - Top-N recommendations effectively capture relevant movies

3. **Neural Network Autoencoder**
   - Architecture: Input → Dense(32) → Latent(4) → Dense(32) → Output
   - Hyperparameters: hidden_size=32, embedding_dim=4, lr=0.001, batch_size=64
   - Achieved Best MAPE = 0.0205
   - Cosine similarity on learned embeddings generates highly relevant similar movies

---

## Results

- Neighborhood-based CF fails to provide meaningful recommendations due to sparsity.
- Matrix Factorization captures latent patterns and provides robust top-N recommendations.
- Autoencoder embeddings outperform traditional CF methods and produce highly accurate movie similarity scores.

---

## Insights & Recommendations

- Use **latent factor models** (Matrix Factorization or Autoencoder) for sparse datasets.
- Combine **content features** for new users or movies (cold-start).
- Leverage **time-aware features** for temporal recommendations.
- Consider **diversity and bias mitigation** (gender, age, niche genres) in recommendations.

---

## Future Work

- Extend to hybrid recommendations combining collaborative and content-based filtering
- Real-time recommendation system integration
- Explore attention-based neural networks for sequential rating patterns
- Incorporate movie metadata like cast, director, and reviews for richer embeddings

---
