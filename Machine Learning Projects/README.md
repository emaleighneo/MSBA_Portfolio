
# Marketing Campaign Analysis

This repository contains code and analysis for a marketing campaign conducted by a Brazilian retail food company. The campaign targeted 2,240 randomly selected customers and aimed to assess the effectiveness of a series of marketing interventions. The company sells products from 5 major categories (wine, rare meat, exotic fruits, specialty fish, and sweets), and the goal is to understand how customers behave based on product type, sales channel, and response to the campaign. 

## Problem Overview

The campaign involved contacting customers via phone 6 times with the goal of selling a particular product. The sales data from this campaign has been provided for analysis. You will learn from this campaign by examining customer purchase behavior and proposing improvements to future marketing efforts.

### Task Breakdown:

1. **Data Preprocessing**:
   - Load and examine the dataset to construct relevant features.
   - Handle missing values, outliers, and any necessary data transformations.

2. **Dimensionality Reduction**:
   - Apply Principal Component Analysis (PCA) to reduce the dimensionality of the dataset.
   - Justify the number of principal components to retain.

3. **Clustering**:
   - Perform clustering based on the principal components, avoiding the use of campaign response in clustering.
   - Determine the optimal number of clusters and explain your choice.
   - Examine how clusters differ in terms of purchasing behavior and campaign response.
   
4. **Profit Calculation**:
   - Calculate the total profit for each cluster.
   - Determine the profit per customer in each cluster as a measure of profitability.
   - Calculate the reach of each cluster (i.e., the percentage of the customer base represented by each cluster).

5. **Predictive Modeling**:
   - Build a predictive model to estimate the total purchases made by a customer in a campaign.
   - Based on the model, create a decision rule to select customers for future campaigns.
   - Calculate the total profit based on the decision rule applied to the test sample.
   - Compare the profitability and reach of the decision rule approach with the clustering-based approach.

## Directory Structure

```plaintext
├── data/
│   └── campaign_data.csv         # Raw data for the marketing campaign
├── notebooks/
│   └── campaign_analysis.ipynb   # Jupyter notebook with detailed analysis and code
├── src/
│   └── preprocess.py             # Preprocessing functions
│   └── pca.py                    # PCA and dimensionality reduction functions
│   └── clustering.py             # Clustering functions (KMeans)
│   └── predictive_model.py       # Predictive model for total purchases
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

## Setup and Installation

To run the analysis, you will need to have Python 3.8 or above installed. Install the required libraries using `pip`:

```bash
pip install -r requirements.txt
```

## Analysis Steps

### 1. Data Preprocessing
The first step is to examine the raw data, check for missing values, and engineer relevant features that could be useful in later analyses.

### 2. Dimensionality Reduction via PCA
Principal Component Analysis (PCA) is applied to reduce the dimensionality of the dataset. The goal is to identify the key components that explain the most variance in customer behavior and reduce the feature space.

We justify the number of components to retain based on the cumulative explained variance ratio.

### 3. Clustering Customers
Using the principal components, we apply clustering algorithms (like K-Means) to group customers based on their purchasing behavior. We will evaluate different values for the number of clusters using metrics such as the silhouette score.

### 4. Cluster Analysis
Once clusters are formed, we compare them in terms of:
   - Their purchase behavior (e.g., how much they purchased).
   - Their response to the marketing campaign (e.g., how many customers in each cluster made a purchase).
   - Their reaction to discounts.

### 5. Profit Calculation
For each cluster, we calculate the total profit generated. The profit from each product sold is given as $3.67. The cost of contacting each customer is $3, so the profit per customer can be computed. Additionally, we calculate the percentage of the customer base that belongs to each cluster.

### 6. Predictive Modeling
A predictive model is built to estimate the number of purchases made by each customer in the campaign. We use regression models (such as linear regression or a more advanced model) and then create a decision rule for selecting customers for future campaigns.

### 7. Decision Rule Evaluation
We apply the decision rule based on our predictive model and evaluate the total profit generated, the profit per customer invited to the campaign, and the percentage of customers invited. This evaluation is then compared to the clustering-based approach.

## Requirements

This project uses the following libraries:

- `pandas` for data manipulation
- `numpy` for numerical operations
- `matplotlib` and `seaborn` for visualization
- `sklearn` for machine learning algorithms (PCA, K-Means, regression models)
- `scipy` for statistical analysis

## Contributing

Feel free to fork the repository, submit issues, or create pull requests if you'd like to contribute. 

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

This project was inspired by marketing data analysis challenges in retail industries. Special thanks to the authors of the libraries and tools used in the analysis.
