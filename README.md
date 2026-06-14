# 🎬 MovieLens Recommendation System

## Overview

This project implements a complete movie recommendation system using the MovieLens 1M dataset. The goal is to help users discover movies they are likely to enjoy by analyzing historical rating patterns and user preferences.

The project follows the full Data Science workflow:

* Problem Definition
* Data Collection
* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Model Development
* Model Evaluation
* Model Improvement
* Recommendation Generation

---

## Dataset

**MovieLens 1M Dataset**

Dataset Statistics:

* 1,000,209 Ratings
* 6,040 Users
* 3,952 Movies
* Rating Scale: 1–5 Stars

Dataset Source:

https://grouplens.org/datasets/movielens/1m/

### Required Files

Download the dataset and place the following files in the project directory:

```text
ratings.dat
users.dat
movies.dat
```

---

## Problem Statement

Streaming platforms contain thousands of movies, making it difficult for users to find content that matches their interests.

This project addresses that problem by building recommendation models that predict user preferences and generate personalized movie recommendations.

---

## Exploratory Data Analysis (EDA)

The following analyses were performed:

* Rating Distribution
* Top Rated Movies
* Ratings by Gender
* Ratings by Age Group
* Most Active Users
* Genre Distribution

Key Insights:

* Rating 4 is the most common rating.
* Drama and Comedy dominate the dataset.
* Male users contribute the majority of ratings.
* A small number of users generate a large portion of ratings.
* Popular movies receive significantly more interactions than average movies.

---

## Data Preprocessing

The preprocessing pipeline includes:

* Merging dataset files
* Duplicate removal
* Missing value verification
* User-Item Matrix creation
* Sparsity handling
* Train-Test Split (80/20)

---

## Recommendation Models

### 1. Popularity-Based Recommendation

Movies are ranked according to average ratings and popularity.

**Advantages**

* Simple
* Fast
* Effective for new users

**Limitations**

* Not personalized

---

### 2. Collaborative Filtering

Uses cosine similarity between users to recommend movies based on similar user behavior.

**Advantages**

* Personalized recommendations

**Limitations**

* Sensitive to sparse data

---

### 3. SVD Matrix Factorization

Uses Singular Value Decomposition (SVD) to uncover latent factors hidden within user-item interactions.

**Advantages**

* Best predictive performance
* Captures hidden user preferences

**Limitations**

* Higher computational cost

---

## Model Evaluation

Evaluation Metrics:

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)

| Model                    | RMSE  | MAE   |
| ------------------------ | ----- | ----- |
| Popularity-Based         | ~1.10 | ~0.88 |
| Collaborative Filtering  | ~0.98 | ~0.78 |
| SVD Matrix Factorization | ~0.89 | ~0.70 |

🏆 **Best Model: SVD Matrix Factorization**

---

## Model Improvement

Different latent factor values were tested:

| Latent Factors | RMSE  |
| -------------- | ----- |
| 20             | ~0.96 |
| 50             | ~0.92 |
| 100            | ~0.89 |

The model with **100 latent factors** achieved the best performance.

---

## Example Recommendation Output

For User 25:

| Rank | Movie                           | Predicted Rating |
| ---- | ------------------------------- | ---------------- |
| 1    | Schindler's List (1993)         | 4.87             |
| 2    | The Shawshank Redemption (1994) | 4.81             |
| 3    | The Silence of the Lambs (1991) | 4.76             |
| 4    | GoodFellas (1990)               | 4.71             |
| 5    | Pulp Fiction (1994)             | 4.68             |

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Scikit-Learn
* Jupyter Notebook

---

## Repository Structure

```text
MovieLens-Recommendation-System/
│
├── MovieLens_Recommendation_System_Final_Project.ipynb
├── MovieLens_Project_Report.docx
├── MovieLens_Presentation.pptx
├── README.md
└── data/
    └── dataset_instructions.md
```

---

## Future Improvements

* Neural Collaborative Filtering
* Autoencoders
* Hybrid Recommendation Systems
* Real-Time Recommendation Pipelines
* Rich Movie Metadata Integration

---

## Author

Arab Academy for Science, Technology & Maritime Transport

College of Computing and Information Technology

Final Data Science / Machine Learning Project
