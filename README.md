# 🎬 Movie Rating Prediction System

📎 [Open in Google Colab](https://colab.research.google.com/drive/1vs5rINGS_legBu_gXPzj02hIA2pdRPEV?usp=sharing)

This project involves building a movie rating prediction and recommendation system using user demographic data, movie metadata, and collaborative filtering techniques. The objective is to analyze user preferences and predict ratings or recommend top movies.

---

## 🧠 Problem Statement

The goal is to predict how a user would rate a movie based on their age, occupation, and historical preferences. Additionally, the project aims to recommend movies a user is likely to enjoy using collaborative filtering techniques.

---

## 📊 Dataset

The project uses three main datasets:
- `Movie RP.txt` – Contains movie details (`MovieNo`, `Title`, `Genres`)
- `Movie RP Ratings.txt` – Includes user ratings (`MovieID`, `Rating`, `Timestamp`)
- `Movie RP User.txt` – User data (`UserId`, `Sex`, `Age`, `Occupation`, `Zip-code`)

All files are delimited using `::`.

---

## 🔧 Tools & Libraries

- Python (pandas, numpy, matplotlib, seaborn)
- Scikit-learn
- Surprise (SVD Collaborative Filtering)
- Jupyter Notebook

---

## 📈 Project Workflow

### 1. Data Cleaning
- Loaded and merged user, movie, and rating data
- Removed missing values
- Ensured consistent column formats for merging

### 2. Exploratory Data Analysis (EDA)
- Analyzed rating distributions
- Visualized movies with high and low ratings
- Identified patterns in user preferences

### 3. Predictive Modeling

#### 📌 Linear Regression
- Used user demographics (`Age`, `Occupation`) to predict movie ratings
- Evaluated using RMSE, MSE, and R² score

#### 📌 Collaborative Filtering (SVD – Surprise Library)
- Built a recommendation model using `UserId`, `MovieID`, and `Rating`
- Trained on 80% of the data and tested on the remaining 20%
- Evaluated performance using RMSE

### 4. Movie Recommendation
- For a given user (e.g., User 1), recommended top 10 movies the user has not rated yet
- Sorted by predicted rating using the SVD model

---

## 🧪 Results

### 📊 Linear Regression (Demographic-based Prediction)
- **RMSE**: 1.0910 
- **R² Score**: 0.14  
(Shows limited predictive power using just age and occupation)

### ⭐ SVD Collaborative Filtering
- **RMSE**: 1.09  
- Recommended personalized movies for users with high predicted ratings

---

## 💡 Sample Output

**Top 10 Movie Recommendations for User 1:**

1. Raiders of the Lost Ark (1981)
2. Last Days of Disco, The (1998)
3. Lawrence of Arabia (1962)
4. Good Will Hunting (1997)
5. Producers, The (1968)
6. On Golden Pond (1981)
7. Graduate, The (1967)
8. Kramer Vs. Kramer (1979)
9. Fantasia (1940)
10. Notorious (1946) 
...

---
