# K-Means Clustering — Student Screen Time vs CGPA

## Overview
This project applies K-Means clustering on a student dataset to identify distinct groups of students based on their screen time habits and academic performance. It was completed as part of a university machine learning course assignment.

## Dataset
- **Source:** [Student Screen Time vs CGPA Analysis 2026](https://www.kaggle.com/datasets/rishisukumar/student-screen-time-vs-cgpa-analysis-2026) (Kaggle)
- **Records:** 546 students
- **Features:** Age, Gender, daily screen time hours, social media hours, online study hours, gaming hours, sleep hours, attendance percentage, offline study hours, previous semester CGPA, current semester CGPA

## Project Structure
```
K-Means_Clustering.ipynb   # Main notebook with all code and analysis
README.md                  # Project documentation
```

## Steps Performed
1. **Data Loading** — Downloaded dataset directly via `kagglehub`
2. **Preprocessing** — Label encoded Gender, dropped redundant features
3. **Exploratory Data Analysis** — Histograms, boxplots, scatter plots, correlation heatmap
4. **Feature Selection** — Selected 5 non-redundant numeric features for clustering
5. **Standardization** — Applied `StandardScaler` to normalize features
6. **Optimal K Selection** — Used Elbow Curve, Silhouette Score, and Calinski-Harabasz Score
7. **K-Means Clustering** — Fitted final model with K=3, n_init=25, random_state=42
8. **Cluster Visualization** — Scatter plot with centroids
9. **Cluster Profiling** — Interpreted each cluster based on feature means

## Features Used for Clustering
- `daily_screen_time_hours`
- `online_study_hours`
- `sleep_hours`
- `attendance_percentage`
- `current_sem_CGPA`

## Results
The optimal number of clusters was determined to be **K=3**, confirmed by all three evaluation methods:

| Method | Optimal K |
|---|---|
| Elbow Curve (WCSS) | K=3 |
| Silhouette Score | K=3 (0.5588) |
| Calinski-Harabasz Score | K=3 (1658.96) |

### Cluster Profiles
| Cluster | Size | Avg Screen Time | Avg CGPA | Profile |
|---|---|---|---|---|
| 0 | 176 | 6.95 hrs | 7.40 | Average Students |
| 1 | 166 | 4.94 hrs | 8.78 | High Performers |
| 2 | 204 | 9.01 hrs | 6.12 | Struggling Students |

## Requirements
```
pandas
numpy
matplotlib
seaborn
scikit-learn
kagglehub
```

Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn kagglehub
```

## How to Run
1. Clone the repository
2. Install the required libraries
3. Open `K-Means_Clustering.ipynb` in Jupyter Notebook or VS Code
4. Run all cells from top to bottom

## Author
Student Assignment — Machine Learning Course 2026
