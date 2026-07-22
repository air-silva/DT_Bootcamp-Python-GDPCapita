# Global GDP per Capita Analysis Using Python

## Background
The [dataset](https://www.kaggle.com/datasets/rajkumarpandey02/gdp-in-usd-per-capita-income-by-country) contains GDP estimates from multiple sources (UN, IMF, World Bank), along with regional classifications and metadata. 
The goal of this exercise was not to answer a specific question, but to practise exploring a real‑world dataset and uncover meaningful patterns.

Full analysis contained in Jupyter/colab notebook. 

### Tools & Libraries
- Python
- Pandas
- Matplotlib
- Seaborn
- NumPy
- Google Colab
-------------------------------------
## Overview
1. Exploratory Data Analysis (EDA)
   - Initial inspection
   - Sorting and ranking
   - Grouping
     
2. Data cleaning & transformation
    - Replacing zero values (with NaN to avoid skewing averages)
    - Checking and filling missing values
    - Dropping temporary columns
      
3. Visualisations
    - Histograms
      - Distribution of IMF, UN, and World Bank estimates
    - Correlation heatmaps
      - Correlation matrices were plotted using Seaborn
    - Bar plots
      - GDP estimates by region
    -  Scatter Plot
      - Comparing UN Region and UN Estimate
    -  Boxplots & Outliers
      
4. Outlier handling
    - Using the IQR method
      - Lower quartile (Q1)
      - Upper quartile (Q3)
      - IQR = Q3 − Q1
      - Upper & lower boundaries calculated
      - Outliers removed to create `df_filtered` - filtered dataset was compared against the original to observe changes in mean GDP values.

## Few Key Insights
- GDP estimates vary widely across regions, with Europe and North America showing the highest values.
- Several countries have missing or zero IMF estimates, requiring imputation.
- UN, IMF, and World Bank estimates are strongly correlated.
- Outliers significantly inflate global averages; removing them provides a more realistic picture of GDP distribution.
- Some regions (e.g., Africa) have many countries below global averages, highlighting global inequality.
