# Fresh-Retail
Building ML models to forecasting sale of Fresh Retail business with latend demand due to stock out

## Overview
The Project is structured into several key sections:
1.  **Setup and Data Download**: Installs necessary libraries and downloads the `FreshRetailNet-50K` dataset from Hugging Face. **Dataset**: [Dingdong-Inc/FreshRetailNet-50K](https://huggingface.co/datasets/Dingdong-Inc/FreshRetailNet-50K)
2.  **Data Preparation**: Cleans and transforms the raw data, creating unique series IDs and day indices.
3.  **Shared Functions**: Defines and applies common data processing functions, including `flag_censoring` (to identify stockouts), `make_features` (for lags and rolling means), and `time_split` (to separate training and validation data).
4.  **Data at a Glance**: Provides a high-level summary and initial visualizations of the dataset characteristics.
6.  **Benchmark with baseline models**: Implemented a Weighted Absolute Percentage Error (WAPE) evaluation function.
Established naive forecasting baselines (Global mean, Seasonal naive, Rolling 28-day) on raw sales and evaluated their performance (D1). Explored a recovery-first approach by imputing censored hourly sales using random pool sampling to estimate corrected daily sales (D2).
7.  **ML models and recovering strategies**: 
