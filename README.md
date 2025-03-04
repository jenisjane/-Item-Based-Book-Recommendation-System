# -Item-Based-Book-Recommendation-System

## Overview
This project builds an **item-based book recommendation system** using **collaborative filtering** with **k-Nearest Neighbors (kNN)**. The goal is to recommend books based on user preferences by analyzing book ratings and finding similar books.

Unlike content-based filtering (which uses book descriptions, genres, or authors), **collaborative filtering** relies on user interactions—suggesting books based on other users with similar preferences.

---

## 🤖 What is k-Nearest Neighbors (kNN)?   
**K-Nearest Neighbors (KNN)** is a simple way to classify things by looking at what’s nearby. 

Imagine a streaming service wants to predict if a new user is likely to cancel their subscription (churn) based on their age. They checks the ages of its existing users and whether they churned or stayed. If most of the “K” closest users in age of new user canceled their subscription KNN will predict the new user might churn too. 

The key idea is that users with **similar ages tend to have similar behaviors and KNN uses this closeness to make decisions**. In this project, kNN helps find books similar to a given book based on user ratings. 

### 🔹 How does kNN work for recommendations?  
1. Convert the dataset into a **user-item matrix**, where rows represent users and columns represent books.  
2. Compute the **similarity** between books using **Cosine Similarity**, which measures how closely two books are rated by users.  
3. Find the **k-nearest books** (most similar books) using **kNN’s kneighbors() function**.  
4. Recommend books that have the highest similarity scores.

---

## 🔍 Methodology  

### 1️⃣ Data Preprocessing  
- **Loaded three datasets:** books, ratings, and user demographics.  
- **Cleaned missing values and inconsistencies** (e.g., invalid publication years).  
- **Filtered users with at least 200 ratings** and **books with at least 100 ratings** to improve accuracy.  

### 2️⃣ Building the Recommendation System  
- **Merged books and ratings datasets** while handling duplicate book titles and ISBNs.  
- **Created a user-item matrix** to represent interactions between users and books.  
- **Converted the matrix into a sparse format** for optimized performance.  

### 3️⃣ Applying kNN for Book Recommendations  
- **Computed Cosine Similarity** to measure book similarity.  
- Used **kNN’s kneighbors() function** to find the most similar books.  
- Randomly selected a book and generated **top book recommendations** based on its similarity to others.  

---

## 🚀 Key Technologies Used  
- **Python** (pandas, NumPy, scikit-learn)  
- **k-Nearest Neighbors (kNN)**  
- **Cosine Similarity**  
- **Exploratory Data Analysis (EDA)**  
- **Sparse Matrix Optimization**  

---

## References  
- [GeeksforGeeks - k-Nearest Neighbours (kNN)](https://www.geeksforgeeks.org/k-nearest-neighbours/)  

