## 🎧Spotify Songs’ Genre Segmentation and Recommendation System

## Project Overview
This project uses a Spotify dataset to perform genre segmentation and build a simple music recommendation system using machine learning. The analysis is based on audio features such as danceability, energy, loudness, tempo, and more.  
The project focuses on:

- Data preprocessing  
- Exploratory data analysis  
- Correlation analysis  
- Clustering using K-Means  
- Dimensionality reduction using PCA  
- Building a similarity-based recommendation engine  

---

## Dataset
The dataset contains more than 32,000 tracks with the following information:

- Track details: `track_name`, `track_artist`, `track_popularity`  
- Playlist metadata: `playlist_name`, `playlist_genre`, `playlist_subgenre`  
- Audio features: `danceability`, `energy`, `loudness`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`, `duration_ms`  
- `track_album_release_date`  

---

## Data Preprocessing
The preprocessing steps performed include:

- Removing duplicate rows  
- Handling missing data  
- Converting album release dates to datetime  
- Selecting numerical features for modeling  
- Scaling audio features using StandardScaler  

---

## Exploratory Data Analysis
The following visualizations were created to understand the dataset:

- Genre distribution  
- Track popularity by genre  
- Tempo distribution  
- Loudness vs energy  
- Danceability vs energy  
- Acousticness vs instrumentalness  
- Correlation heatmap  
- Cluster distribution by playlist genre  
- Playlist-level cluster distribution  

These analyses help reveal patterns across genres and audio features.

---

## Clustering
K-Means clustering was applied to group songs with similar audio characteristics.

### Steps:
1. Selecting relevant features  
2. Standardizing the data  
3. Using PCA to reduce dimensions to 2 components  
4. Running K-Means with different K values  
5. Using Silhouette Score to select the best K  

The optimal number of clusters was determined to be:

## k = 2

Useful for playlist continuation



The clusters were visualized using PCA scatter plots.

---

## Recommendation System
A simple recommendation system was implemented using Nearest Neighbors.

Given a track index, the model returns a list of similar songs based on audio features. This can be used for playlist continuation or music discovery.

Example output includes `track_name`, `track_artist`, and `playlist_genre`.

---


---

## Technologies Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-Learn  
- Jupyter Notebook  

---

## How to Run the Project
1. Clone the repository:
2. install dependencies
3. open the notebook 
4. Run all cells to reproduce the results.

---

## Key Findings
- Two major clusters naturally emerge from Spotify audio features.  
- Genres like pop, edm, and rap show distinct feature patterns.  
- PCA effectively visualizes clusters in 2 dimensions.  
- The recommendation system can find similar songs based on feature similarity.  

---

## Future Improvements
- Use advanced clustering methods such as DBSCAN or Gaussian Mixture Models  
- Build a deep learning recommendation model  
- Deploy the pipeline as a web-based application  
- Integrate the Spotify API to fetch real-time track data  
