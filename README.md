# 📚 Book Recommendation System

### 🚀 Live Project Overview

A Machine Learning-based Book Recommendation System that provides personalized book suggestions using multiple recommendation techniques including Collaborative Filtering, Content-Based Filtering, Popularity-Based Recommendation, and Hybrid Models.

---

## 📖 Description

This project aims to help readers discover books tailored to their interests by leveraging user ratings, book metadata, and machine learning algorithms. The system analyzes user preferences and recommends books based on popularity, similarity, and historical interactions.

### Dataset

The dataset consists of three primary tables:

* **Books**
* **Users**
* **Ratings**

The dataset was obtained from the Book-Crossing Dataset and underwent extensive preprocessing before model development.

---

# 1. Data Cleaning & Preprocessing

## Books Dataset

* Removed image URL features.
* Handled missing values by replacing null entries with appropriate values.
* Corrected inconsistent publication year records.
* Standardized ISBN formatting.
* Removed duplicate records.
* Converted publication years into integer format.
* Replaced invalid publication years with statistically appropriate values.

## Users Dataset

* Processed missing age values.
* Removed unrealistic age entries.
* Replaced invalid ages using mean age imputation.
* Extracted City, State, and Country from location information.
* Handled missing location values.
* Removed duplicate user records.

## Ratings Dataset

* Validated ISBN integrity.
* Standardized ISBN formatting.
* Removed invalid and duplicate ratings.
* Ensured numerical consistency in User-ID and Rating fields.

---

# 2. Recommendation Algorithms Implemented

## 2.1 Popularity-Based Recommendation

### Popular Books Overall

Books are ranked according to:

* Total ratings received
* Average user ratings
* Popularity score

### Popular Books by Location

Recommendations are generated based on:

* City
* State
* Country

### Author & Publisher-Based Recommendation

Recommends highly rated books from:

* Same Author
* Same Publisher

### Year-wise Popular Books

Identifies top-rated books for each publication year.

---

## 2.2 Weighted Average Rating Recommendation

Weighted rating score is calculated using:

score = (t/(t+m)) × a + (m/(m+t)) × c

Where:

* **t** = Total ratings received by a book
* **m** = Minimum ratings threshold
* **a** = Average rating of the book
* **c** = Mean rating across all books

Books with the highest weighted scores are recommended.

---

## 2.3 User-Item Collaborative Filtering

Collaborative Filtering identifies similar user preferences using:

* User-Book Interaction Matrix
* Cosine Similarity
* Rating Patterns

Recommendations are generated based on books liked by users with similar interests.

---

## 2.4 Correlation-Based Recommendation

This approach:

* Builds a User-Book Rating Matrix
* Computes correlation scores between books
* Recommends highly correlated books

---

## 2.5 K-Nearest Neighbors (KNN) Recommendation

Implemented using:

* Sparse User-Book Matrix
* Cosine Distance Metric
* Nearest Neighbors Algorithm

The model finds books most similar to the selected book.

---

## 2.6 Content-Based Recommendation

Content similarity is calculated using:

* TF-IDF Vectorization
* Unigrams & Bigrams
* Cosine Similarity

Recommendations are based on book title similarity and content features.

---

## 2.7 Hybrid Recommendation System

A hybrid model combining:

* Collaborative Filtering
* Content-Based Filtering

Benefits:

* Improved recommendation accuracy
* Reduced cold-start problem
* Better personalization

---

# 3. Technologies & Libraries Used

### Programming Language

* Python

### Machine Learning

* Scikit-Learn
* SciPy

### Data Analysis

* Pandas
* NumPy

### Visualization

* Matplotlib
* Seaborn

### Development Environment

* Jupyter Notebook

---

# 4. Project Features

✅ Personalized Book Recommendations

✅ Popular Books Discovery

✅ Author-Based Recommendations

✅ Publisher-Based Recommendations

✅ Location-Based Recommendations

✅ Content Similarity Search

✅ Collaborative Filtering Engine

✅ Hybrid Recommendation System

✅ Data Visualization & Insights

---

# 5. Future Enhancements

* User Authentication System
* Real-Time Recommendation Engine
* Deep Learning-Based Recommendations
* Streamlit Web Application
* Book Cover Integration
* User Review Analysis using NLP
* Cloud Deployment

---

# 6. Results

The hybrid recommendation model demonstrated superior recommendation quality by combining user preference patterns with content similarity, leading to more relevant and personalized book suggestions.

---

## 👨‍💻 Author

**Manish Bairwa**

B.Tech AI&DS | Data Science & Machine Learning Enthusiast

Connect with me on LinkedIn and GitHub for collaboration and project discussions.
