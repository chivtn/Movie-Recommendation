# 🎬 Movie Recommendation System

A **data-driven recommendation system** that predicts user preferences and suggests movies using **Content-Based Filtering**, **User-User Collaborative Filtering**, and **Item-Item Collaborative Filtering**.

This project was built as part of the **Data Analysis course** at **Ho Chi Minh City Open University (OU)**.

---

## 📌 Overview

In the digital era, streaming platforms like **Netflix** or **Amazon Prime** contain millions of movies, making it difficult for users to choose the right content.

A **Recommendation System** personalizes user experiences, increases satisfaction, and improves customer retention.

This project applies **machine learning techniques** on the MovieLens dataset to build a movie recommendation system.

---

## 🎯 Objectives

- Apply **data analysis** and **machine learning** in practice.  
- Explore **preprocessing**, **visualization**, and **model evaluation** for recommender systems.  
- Compare different algorithms:
  - **Content-Based Filtering (CBF)**
  - **User-User Collaborative Filtering (UCF)**
  - **Item-Item Collaborative Filtering (ICF)**

---

## 📂 Dataset

**Source:** MovieLens `ml-latest-small`

### Files Used
- **movies.csv** — 9,743 movies (movieId, title, genres)  
- **ratings.csv** — 100,837 ratings (610 users, scale 1–5)

---

## ⚙️ Data Processing

### ✔ Cleaning  
- Handle missing values  
- Remove duplicates  
- Normalize text formatting  

### ✔ Merging  
- Combine movies & ratings into a single dataframe  

### ✔ Feature Engineering  
- Extract and encode genres  
- Apply **TF-IDF vectorization**  
- Encode userId/movieId for sparse matrix usage  

### ✔ Outlier Handling  
- Weighted rating using **Bayesian Average**

---

## 📊 Visualization Insights

- Most ratings fall between **3.0–4.5**, showing positive bias.  
- Majority of users provide fewer than **100 ratings**.  
- Most movies receive fewer than **50 ratings**.  
- Popular movies tend to have **higher average ratings**.

---

## 🤖 Models Implemented

### 1️⃣ Content-Based Filtering (CBF)
- TF-IDF on genres  
- Ridge Regression for rating prediction  
- **RMSE: 0.9119**

---

### 2️⃣ User-User Collaborative Filtering (UCF)
- Cosine similarity between users  
- Predict using k-nearest neighbors  
- **RMSE: 0.1021 → Best performance**

---

### 3️⃣ Item-Item Collaborative Filtering (ICF)
- Compute similarity between movies  
- Recommend based on user history  
- **RMSE: 0.3893**

---

## 📈 Evaluation

- **Metric:** RMSE (Root Mean Squared Error)  
- **Best Model:** User-User Collaborative Filtering  
- **Limitations:**  
  - CBF lacks diversity  
  - ICF suffers from data sparsity  
- **Future Work:** Build a **Hybrid Recommendation System**



## 🗂️ Project Structure

