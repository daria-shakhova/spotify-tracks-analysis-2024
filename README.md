# Spotify Top Tracks 2024: Cross-Platform Analysis & Radio Bias Study

**Comprehensive analysis of music streaming metrics** revealing platform-specific patterns and statistically significant content-based biases in radio programming.
You can explore my Python code via the [Colab link](https://colab.research.google.com/drive/1TPeqFPINMvV5FcG0K3GWMPEQDb8Yj9le?usp=sharing).

## 📊 Project Overview

This project analyzes Spotify's "Top Tracks 2024" dataset combined with metrics from Apple Music, YouTube, and TikTok. Through exploratory data analysis and statistical testing, we investigate:

- **Cross-platform correlations** between different engagement metrics
- **Factors predicting track quality** (Track Score)
- **Content-based biases** in radio airplay distribution
- **Temporal trends** in music perception over the past decade

## 🎯 Key Findings

### 1. 📻 Radio Programming Bias
- **Child-friendly tracks receive more radio airplay** than explicit tracks
- **Statistically significant** (Fisher's exact test: p < 0.05)
- Confirmed by both visualization (box plots) and hypothesis testing

### 2. 🔗 Platform Correlation Patterns
- **TikTok operates independently** from other platforms (weak correlations)
- **YouTube shows strong internal consistency** (views ↔ likes: ρ = 0.83)
- **Apple Music correlates moderately** with multiple platforms:
  - Radio airplay (Airplay Spins): ρ = 0.58
  - Spotify Playlist Count: ρ = 0.69
  - Spotify Playlist Reach: ρ = 0.67

### 3. 🎵 Track Quality Predictors
- **Spotify Playlist Reach correlates strongest with Track Score** (Spearman's ρ = 0.50)
- **Apple Music Playlist Count** is the second strongest predictor
- The relationship **approximates linearity** (significant Pearson's r)

### 4. 📈 Temporal Trends
- **Post-2015 tracks score significantly higher** than pre-2015 releases
- Suggests either quality improvement or rating inflation over time

### 5. 📅 Dataset Characteristics
- **Covers first half of 2024** (latest track: June 14, 2024)
- **Low-scoring tracks predominate** (Track Score < 250)
- **Non-explicit tracks constitute majority** 

## 🛠️ Technical Implementation

### Data & Tools
- **Dataset**: [Spotify 2024 Tracks Dataset](https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024) on Kaggle 
  (includes metrics from Spotify, Apple Music, YouTube, and TikTok)
- **Languages**: Python 3.8+
- **Libraries**: pandas, NumPy, SciPy, matplotlib, seaborn, statsmodels
- **Environment**: Jupyter Notebook

### Analytical Methods
1. **Exploratory Data Analysis (EDA)**
   - Data cleaning and validation
   - Distribution analysis
   - Missing value handling

2. **Statistical Analysis**
   - **Correlation analysis**: Spearman's ρ (monotonic), Pearson's r (linear)
   - **Hypothesis testing**: Fisher's exact test, Mann-Whitney U test
   - **Regression analysis**: Linear model fitting

3. **Data Visualization**
   - Box plots for distribution comparison
   - Scatter plots with regression lines
   - Heatmaps for correlation matrices
   - Bar charts for categorical comparisons
