# Hybrid Recommendation System for E-Commerce

![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-orange)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3%2B-green)

A hybrid recommendation system combining **collaborative filtering** (user behavior) and **content-based filtering** (product features) to deliver personalized product recommendations for online retail. The system cleans raw transaction data, analyzes purchase patterns, and leverages product descriptions to generate recommendations.

---

## Features
- **Data Preprocessing**: Handles missing values, negative quantities, and duplicates, then aggregates user-item interactions into a pivot table.  
- **Collaborative Filtering**: Uses cosine similarity on normalized purchase data (`StandardScaler`) to find users with similar behaviors.  
- **Content-Based Filtering**: Applies TF-IDF vectorization to product descriptions and computes semantic similarity.  
- **Hybrid Model**: Combines both approaches with adjustable weights (e.g., `70% collaborative + 30% content-based`) for balanced recommendations.  

---

## How It Works
- **Data Cleaning: Raw data is scrubbed by removing orders with negative quantities/zero prices and deduplicating product descriptions.

- **Collaborative Filtering: A user-item pivot table (quantities purchased) is created, normalized with StandardScaler, and analyzed using cosine similarity to identify similar users.

- **Content-Based Filtering: Product descriptions are vectorized using TfidfVectorizer, and cosine similarity identifies semantically similar items.

- **Hybrid Recommendations: Scores from both methods are combined with configurable weights (e.g., weight_collab=0.7, weight_content=0.3) to generate final recommendations.
