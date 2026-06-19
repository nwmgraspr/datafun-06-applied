# Netflix Titles EDA Project

## Author
Ralph Massaquoi  
Date: June 2026

---

##  Overview

This project performs exploratory data analysis (EDA) on the Netflix Titles dataset using Python. 
The goal is to clean, analyze, and visualize Netflix movies and TV shows to discover patterns and insights.

---

##  Dataset

- Source: `data/raw/netflix_titles.csv`
- Contains information about Netflix movies and TV shows including:
  - title
  - type (Movie or TV Show)
  - director
  - cast
  - country
  - date added
  - release year
  - rating
  - duration
  - genre

---

##  Features of the Project

This script (`app_case.py`) performs:

### 1. Data Loading
- Loads CSV file using pandas

### 2. Data Cleaning
- Converts `duration` into numeric minutes
- Converts `date_added` to datetime
- Creates new feature: `year_added`

### 3. Data Exploration
- Displays dataset shape and structure
- Checks missing values and duplicates
- Builds a data dictionary

### 4. Statistical Analysis
- Summary statistics using pandas and NumPy
- Grouped analysis by content type

### 5. Correlation Analysis
- Creates correlation matrix for numeric columns
- Visualizes results using a heatmap

### 6. Data Visualization
- Scatter plot: Release Year vs Duration
- Box plot: Duration by Type (Movie vs TV Show)

---

## Key Insights

- Netflix content trends over time
- Differences between Movies and TV Shows
- Distribution of content duration
- Relationships between numeric variables

---

## How to Run

From the project root folder:

```bash
uv run python -m datafun.app_case
