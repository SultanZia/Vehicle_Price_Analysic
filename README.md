
**Overview**

This project analyzes a real-time dataset of 400,000 used vehicles from Auto Trader, extracted via SQL, to explore pricing trends in the UK market. With 14 columns and significant data challenges (>10% missing values, >25% noise), I applied Exploratory Data Analysis (EDA), feature engineering, and preprocessing to uncover patterns and ensure data quality. This work showcases my ability to wrangle large, messy datasets and derive insights using Python, making it a valuable addition to my portfolio for job applications.


**Objectives**
Visualize and analyze factors influencing vehicle prices.
Enhance data understanding through feature engineering and EDA.
Clean and preprocess a noisy, real-world dataset.

**Dataset**
Source: Auto Trader (UK), extracted using SQL.
Size: 400,000 rows, 14 columns.
Features: Includes mileage (float), reg_code (object), standard_make (e.g., Renault), standard_model (e.g., Captur), year_of_registration, body_type, fuel_type, vehicle_condition, standard_colour, and others.


**Challenges:**
Over 10% missing values (NaN).
Over 25% noise: outliers, incorrect entries (e.g., future year_of_registration), and human errors.


**Methodology**
**1. Exploratory Data Analysis (EDA)**
Distributions: Histograms for mileage and boxplots to identify outliers.
Relationships: Scatter plots (mileage vs. price) and bar charts (price by standard_make/standard_model).
Categorical Analysis: Count plots for body_type and fuel_type.
Tools: Pandas, Matplotlib, Seaborn.

**2. Feature Engineering**
Age Calculation: Derived a new feature, age, as 2021 - year_of_registration to capture vehicle age, enhancing temporal analysis.
Standardization: Scaled numerical features like mileage for consistency.
Categorical Encoding: Transformed standard_make and standard_model into numerical formats for deeper analysis.

**3. Data Preprocessing**
Missing Values: Imputed with median (numerical, e.g., mileage) and most frequent (categorical, e.g., fuel_type).
Outliers: Treated extreme mileage values via boxplot-guided replacement or removal.
Noise: Corrected errors in reg_code and year_of_registration using replace() and map().

**Key Insights**
Mileage Impact: Correlation analysis showed a weak negative relationship (-0.052344) between mileage and price, confirmed by scatter plots.
Age Effect: Vehicles with older year_of_registration (higher age) showed a slight positive correlation (0.021617) with price, possibly due to vintage value, per correlation data.
Data Quality: Boxplots revealed significant outliers in mileage, necessitating preprocessing to address >25% noise.

**Repository Contents**
vehicle_price_analysis_eda.ipynb: Jupyter Notebook with SQL extraction, EDA, feature engineering, and preprocessing.

**Visualizations**
Scatter Plot: mileage vs. price for correlation.
Boxplot: mileage outlier detection.
Bar Chart: Average price by standard_make.
Count Plot: Frequency of body_type.


