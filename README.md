# NYC Taxi Trip Data Analysis

An exploratory data analysis project investigating New York City taxi trips using Python, statistical analysis, geospatial techniques, and dimensionality reduction.

The project analyses taxi trip data to identify temporal patterns, geographic hotspots, airport travel trends, and potential groups of trips with similar characteristics.

## Project Overview

This project uses the NYC Taxi Trip Duration dataset to investigate how taxi usage varies by time, location, trip distance, and other characteristics.

The analysis covers data cleaning, feature engineering, temporal patterns, geographic clustering, airport journeys, and dimensionality reduction.

## Objectives

- Identify and justify the removal of anomalous taxi trips.
- Engineer features such as trip distance, day of the week, and average speed.
- Investigate taxi demand across days, hours, weekends, and major holidays.
- Explore pickup locations using geographic heatmaps.
- Identify pickup hotspots using DBSCAN clustering.
- Compare travel times to JFK and Newark airports from the Empire State Building.
- Explore trip patterns using PCA, t-SNE, and UMAP.
- Apply density-based clustering to reduced feature spaces and compare the resulting clusters.

## Dataset

The project uses the **NYC Taxi Trip Duration dataset**, available through Kaggle and referenced in the assignment brief.

The dataset contains approximately 1.5 million taxi trips recorded between January and June 2016.

Relevant variables include:

- Trip ID
- Vendor ID
- Pickup and drop-off timestamps
- Passenger count
- Pickup and drop-off coordinates
- Store-and-forward flag
- Trip duration

The analysis uses the training dataset specified in the assignment.

**Dataset source:** [NYC Taxi Trip Duration — Kaggle](https://www.kaggle.com/c/nyc-taxi-trip-duration)

The dataset is not included in this repository unless explicitly added. Follow the dataset provider's terms when downloading and using it.

## Analysis and Methodology

### 1. Data Cleaning

Identify anomalous observations using trip duration, geographic distance, calculated speed, and other relevant variables.

Removal criteria should be justified to distinguish implausible trips from unusual but potentially valid observations.

### 2. Feature Engineering

Generate additional features to support the analysis, including:

- Trip distance using geographic coordinates.
- Day of the week.
- Average trip speed.
- Pickup hour and other time-based features.

### 3. Temporal Analysis

Investigate taxi usage patterns over time by examining:

- The most popular day of the week.
- Hourly demand across different days.
- Differences between weekdays and weekends.
- Changes in demand on selected public holidays.
- Average trip speed throughout the day.

Visualizations are used to communicate patterns and support observations.

### 4. Geospatial Analysis

Explore the geographic distribution of taxi pickups using heatmaps for different time periods, including weekdays, weekends, mornings, and evenings.

Apply DBSCAN to identify pickup hotspots during the specified Friday-night and Thursday-evening periods. Select clustering parameters based on geographic distance and pickup density, and visualize the resulting clusters on a map.

### 5. Airport Travel Analysis

Investigate travel times from the Empire State Building to:

- John F. Kennedy International Airport (JFK).
- Newark Liberty International Airport (EWR).

Estimate average travel times by time of day and compare the observed patterns between the two destinations.

### 6. Dimensionality Reduction

Use a reproducible sample of 20,000 cleaned trips to explore the structure of the feature space.

The analysis includes:

**Principal Component Analysis (PCA)**
- Explained variance and cumulative variance.
- The number of components needed to explain 90% of the variance.
- Principal-component visualizations and feature-loading interpretation.

**t-distributed Stochastic Neighbor Embedding (t-SNE)**
- Comparison of different perplexity values.
- Visualization of potential local structure in the trip data.

**Uniform Manifold Approximation and Projection (UMAP)**
- Comparison of different neighborhood sizes and minimum-distance settings.
- Investigation of how parameter choices affect the resulting embeddings.

### 7. Clustering and Comparison

Apply DBSCAN or HDBSCAN to the reduced feature spaces.

Evaluate the resulting clusters using:

- Number of clusters identified.
- Fraction of trips classified as noise.
- Profiles of original trip features.
- Geographic distributions of cluster members.
- Adjusted Rand Index (ARI) comparisons between clustering results.

Compare PCA, t-SNE, and UMAP in terms of their ability to reveal meaningful patterns, their computational requirements, and their sensitivity to parameter choices.

## Technologies and Libraries

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- GeoPandas
- Folium
- Scikit-learn
- UMAP

## Repository Structure

```text
nyc-taxi-data-analysis/
├── README.md
├── requirements.txt
├── notebooks/
│   └── nyc_taxi_analysis.ipynb
├── reports/
│   └── nyc_taxi_analysis.pdf
└── figures/
    └── ...
```

The structure above is a suggested organization. Adjust it to match the files included in the repository.

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/nyc-taxi-data-analysis.git
cd nyc-taxi-data-analysis
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the Dataset

Download the NYC Taxi Trip Duration dataset from Kaggle and place the training CSV in the location expected by the notebook.

Update the notebook's dataset path if necessary.

### 4. Run the Notebook

Launch Jupyter:

```bash
jupyter notebook
```

Open the analysis notebook and execute the cells in order.

## Deliverables

The project is organized around two main deliverables:

- **Jupyter Notebook:** Documents the data processing, analysis, visualizations, and answers to the assignment questions.
- **PDF Report:** Presents the analysis, plots, interpretations, and conclusions.

## Project Status

Data analysis and exploration.

The repository documents an investigation of NYC taxi trip patterns using temporal analysis, geospatial methods, and dimensionality reduction.
