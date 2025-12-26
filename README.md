# 📊 Customer Segmentation Analysis Project (Mall Customer Segmentation)

<div align="center">
  <img src="output.png" width="500" alt="K-Means Clustering Visualization">
</div>

## Introduction

This project is part of a data analysis case study aimed at identifying distinct customer segments within the **Mall Customer** dataset. By understanding the unique characteristics of each segment, businesses can develop more targeted and personalized marketing strategies, improve customer satisfaction, and maximize profits.

In this project, I applied various basic to intermediate data science techniques, including data loading, exploratory data analysis, feature normalization, and the K-Means Clustering algorithm for segmentation.

## Dataset

The dataset used is the **Mall Customer Dataset**, which contains basic information about shopping mall customers, including:

* `CustomerID`: Unique customer ID
* `Gender`: Customer gender
* `Age`: Customer age
* `Annual Income (k$)`: Customer annual income (in thousands of dollars)
* `Spending Score (1-100)`: Spending score assigned by the mall based on customer purchasing behavior (scale 1–100)

## Project Objectives

1. Load and explore the customer dataset.
2. Perform basic data preprocessing (e.g., checking for missing values, feature normalization).
3. Determine the optimal number of clusters using the Elbow Method.
4. Apply the K-Means Clustering algorithm to segment customers.
5. Analyze and understand the characteristics of each resulting customer segment.
6. Visualize the segmentation results to gain deeper insights.

## Technologies / Libraries Used

* **Python**
* **Pandas**: For data manipulation and analysis.
* **NumPy**: For numerical operations.
* **Scikit-learn (sklearn)**: For data normalization (`MinMaxScaler`) and clustering algorithms (`KMeans`).
* **Matplotlib**: For data visualization.
* **Seaborn**: For enhanced and more attractive data visualizations.

## Analysis Workflow

This project follows a standard data analysis workflow:

1. **Data Loading**: Load the `data.csv` dataset using Pandas.
2. **Initial Data Exploration**:

   * View general dataset information (`.info()`).
   * Check for missing values (`.isnull().sum()`).
   * Generate descriptive statistics (`.describe()`).
   * Visualize age distribution (`histogram`) and gender distribution (`pie chart`).
3. **Data Normalization**: Apply `MinMaxScaler` to numerical features (`Age`, `Annual Income (k$)`, `Spending Score (1-100)`) to ensure all features are on the same scale, which is crucial for distance-based algorithms like K-Means.
4. **Determining the Optimal Number of Clusters (Elbow Method)**:

   * Run the K-Means algorithm for `k` values from 1 to 10.
   * Record the *inertia* (Within-Cluster Sum of Squares) for each `k`.
   * Plot *inertia* vs. `k` to identify the “elbow point” indicating the optimal number of clusters. In this analysis, **k = 5** was selected as the optimal number of clusters.
5. **Customer Segmentation with K-Means**:

   * Apply the K-Means algorithm with `n_clusters = 5`.
   * Assign the resulting cluster labels back to the original DataFrame.
6. **Cluster Profiling**:

   * Analyze the characteristics of each cluster by calculating the mean of numerical features (`Age`, `Annual Income (k$)`, `Spending Score (1-100)`) for each cluster.
   * Examine gender distribution in each cluster using cross-tabulation.
   * Provide interpretations and assign meaningful names to each customer segment (e.g., “Priority Customers,” “Budget Customers,” etc.).
7. **Cluster Visualization**: Create scatter plots to visualize customer segments based on feature combinations (`Annual Income` vs. `Spending Score` and `Age` vs. `Spending Score`), with points colored according to their cluster labels.

## Results and Insights

This analysis successfully identified **five distinct customer segments** with unique characteristics:

* **Cluster 0 (Middle Customers)**: Middle-aged customers with moderate income and spending scores.
* **Cluster 1 (Priority Customers)**: Young to middle-aged customers with high income and high spending scores.
* **Cluster 2 (Budget Customers)**: Middle-aged customers with low income and low spending scores.
* **Cluster 3 (Potential Customers)**: Young to middle-aged customers with high income but low spending scores (high potential for targeted marketing).
* **Cluster 4 (Young & Impulsive Customers)**: Young customers with moderate income and high spending scores.

These insights can be leveraged by marketing teams to:

* Design targeted promotional campaigns for each segment.
* Develop products or services tailored to the specific needs of each group.
* Improve customer retention by better understanding customer preferences.

## How to Run This Project

To run this notebook on your local machine:

1. **Clone this repository:**

   ```bash
   git clone https://github.com/YourUsername/YourRepoName.git
   ```

   *Replace `YourUsername` and `YourRepoName` with your GitHub username and repository name.*
2. **Navigate to the project directory:**

   ```bash
   cd YourRepoName
   ```
3. **Ensure Python and the required libraries are installed.** Install dependencies using:

   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
4. **Open the Jupyter Notebook** (`your_notebook_filename.ipynb`) using Jupyter Lab or Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

   *Replace `your_notebook_filename.ipynb` with your actual notebook file name (e.g., `mall_customer_segmentation.ipynb`).*
5. Run each cell in the notebook sequentially.

---

**Created by:** Khairunnisa Maharani
**Date:** July 26, 2025
