# Customer Segmentation Project (Retail Analytics)
This project analyzes a transnational e-commerce dataset to segment customers into distinct groups.
## Objective
To replicate the project on my resume , which involves segmenting customers into 4 distinct groups to enable data-driven marketing, improve targeting by ~20%, and boost retention by ~15%. 

## Methodology
The project uses the **RFM (Recency, Frequency, Monetary)** model to quantify customer behavior. It then applies **K-Means Clustering** (an unsupervised machine learning algorithm) to partition customers into **k=4** distinct, actionable segment

## Project Structure
- data/: Contains raw and processed data.

  - data/raw/: The 'Online Retail II UCI' dataset.

  - data/processed/: The cleaned, processed RFM data.

- notebooks/: Contains the main analysis notebook.

  - 01_Segmentation_Analysis.ipynb: The main notebook used to import, process, model, and analyze the data.

- scripts/: Contains reusable Python helper functions.

  - data_processing.py: Functions for loading, cleaning, and calculating RFM features.

  - model.py: Functions for scaling data and building the K-Means model.

- results/: Contains final outputs.

  - results/reports/: CSV files of the final cluster profiles.

  - results/plots/: Visualizations of the cluster profiles.

## How to Run
Download the data: Get the 'Online Retail II UCI' dataset from Kaggle and place the online_retail_II.csv file in the data/raw/ folder.

Install dependencies: pip install pandas scikit-learn matplotlib seaborn

Run the analysis: Open the notebooks/01_Segmentation_Analysis.ipynb notebook and run the cells from top to bottom.and run the cells from top to bottom.
