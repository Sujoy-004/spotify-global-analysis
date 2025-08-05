# 🎧 Spotify Global Analysis (EDA + Data Cleaning + Regression Model)

This project performs a detailed analysis of global Spotify listening trends using the `spotify_history.csv` dataset. We explore country-wise listening behaviors, genre popularity, and predictive patterns using machine learning models — culminating in a regression-based popularity prediction model.

---

## 📌 Dataset
- **Source**: [Kaggle - Top Spotify Songs in Countries](https://www.kaggle.com/datasets/anandshaw2001/top-spotify-songs-in-countries)
- **File Used**: `spotify_history.csv`
- **Shape**: 114,000+ rows × 19 columns
- **Data Includes**:
  - Country
  - Track Name
  - Artist Name
  - Position
  - Streams
  - Date & Time
  - Popularity
  - Genre
  - ...more

---

## 🚀 Project Phases

### ✅ Phase A: Setup
- Imported required libraries (`pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`)
- Loaded and briefly inspected the dataset

---

### 📊 Phase B: EDA & Data Cleaning
- Renamed timestamp (`ts`) column to `timestamp` for clarity
- Handled missing values
- Cleaned column names and standardized genres
- Parsed `timestamp` into new features:
  - `hour`
  - `day`
  - `month`
  - `weekday`

**Key Visualizations:**
- Heatmap of missing data
- Top 10 countries by song count
- Genre distribution by country
- Streams vs. Popularity scatterplots

---

### 🔎 Phase C: Feature Engineering
- Extracted features from `timestamp`
- Cleaned outliers in `streams` and `popularity`
- One-hot encoded categorical columns (`genre`, `country`)

---

### 🧠 Phase D: Model Training (Linear Regression)
- Split data into train/test using `train_test_split`
- Trained a basic Linear Regression model on:
  - Features: `hour`, `day`, `streams`, `genre`, `country`
  - Target: `popularity`
- Evaluated using:
  - R² Score
  - Mean Squared Error

---

### 🧪 Phase E: Model Enhancement (XGBoost)
- Switched to `XGBoostRegressor` for improved performance
- Feature importance plotted
- Notable improvement in prediction accuracy

---

### 📈 Phase F: Result Analysis
- Compared Linear Regression and XGBoost
- Discussed shortcomings (low R² on Linear)
- Identified further optimization areas (feature scaling, ensemble methods, deep learning)

---

## 💡 Future Improvements
- Time-series modeling on song popularity trends
- Cluster analysis per country/genre
- Deploy as a dashboard using Streamlit or Flask
- Add song recommendation engine logic

---

## 🛠️ Tech Stack
- **Python** (Pandas, Numpy, Seaborn, Matplotlib, Scikit-learn, XGBoost)
- **Jupyter Notebook (Google Colab)**
- **GitHub** for version control

---

## 📁 Repository Structure
