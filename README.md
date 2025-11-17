# BNPL Merchant Ranking Project
This project develops a data pipeline and ranking system to identify the top-performing Buy Now Pay Later (BNPL) merchants based on multiple business dimensions — profitability, growth potential, customer loyalty, and fraud risk. By integrating multiple data sources and analytical models, the system aims to enhance strategic decision-making for merchant onboarding, partnership prioritization, and fraud management.

## Project Overview:
- This project follows a modular ETL → Modelling → Ranking pipeline designed for scalability, interpretability, and reproducibility.
- Each notebook in the repository represents a distinct stage in the analytical workflow.

**Key Objectives:**
- Build an end-to-end analytical pipeline for BNPL merchant evaluation.
- Model and impute missing fraud probabilities for consumers and merchants.
- Forecast future merchant revenue to estimate growth trajectories.
- Rank merchants using a weighted multi-metric framework incorporating both performance and risk.
- Segment merchants by industry and behavior to uncover actionable insights.

## How to Run:
1. Install dependencies  
   - Run the following command to install all required packages:  
     ```bash
     pip install -r requirements.txt
     ```
2. Run the notebooks in order from 1 to 10.  

   **1. Data Preprocessing**: Prepares and cleans the main and external datasets.  
   - `1_Preprocessing.ipynb` 
   - `1.1_GCP_Preprocessing.ipynb` 
   - `1.2_WPP_Preprocessing.ipynb`
   - `1.3_SEIFA_APRA_Preprocessing.ipynb` 

   **2. Exploratory Data Analysis (EDA)**: Examines dataset coverage, missing values, and feature distributions.  
   - `2_Preliminary_Analysis.ipynb`  
   - `2.1_GCP_EDA.ipynb`  
   - `2.2_SEIFA_APRA_EDA.ipynb`  

   **3–4. Merge Datasets**: Combines internal and external data sources.  
   - `3_Merge_Given_Dataset.ipynb`  
   - `4_Merge_External_Datasets.ipynb`  

   **5. Delta File Creation**: Creates the `is_fraud` flag using rule-based detection.  
   - `5_Delta_File_Creation.ipynb`  

   **6–7. Fraud Modelling**: Predicts missing fraud probabilities for consumers and merchants.  
   - `6_Consumer_Fraud_Model.ipynb`  
   - `7_Merchant_Fraud_Model.ipynb`  

   **8. Revenue Forecasting**: Prepares and forecasts merchant revenue for growth calculation.  
   - `8.1_Revenue_Forecast_Data_Prep.ipynb`  
   - `8.2_Revenue_Forecast.ipynb`  

   **9. Merchant Ranking and Segmentation**: Computes ranking scores and groups merchants into industry segments.  
   - `9_Ranking_Merchants.ipynb`  
   - `9.1_Segmentation_Manual.ipynb`  
   - `9.2_Segmentation_Kmeans.ipynb`  

   **10. Summary**: Consolidates results, assumptions, and recommendations.  
   - `10_Summary.ipynb`

## Output Files:
   - Cleaned and merged datasets
   - Consumer and merchant fraud probability models
   - Revenue growth forecast
   - Final merchant rankings and segment insights

## Contributors:
**Group 25 – BNPL Project**
- Kiesha Alexandra Krisna  
- Felicia Lauretta Gunawan  
- Vivian Karim  
- Ahmad Yasin  
- Emily Joseph
