**Project Description**
This project involves building a linear regression model to predict residential propertyprices based on features such as number of bedrooms, bathrooms, garages, size, and location. This dataset was manually scraped from Property24, a South Africam estate platform. The workflow includes data cleaning, feature engineering, exploratory data analyiss (EDA), visualisations and regression modelling to understand which factors drive property prices and how accurately we can predict them

**Dataset Overview**
Source: Manually scraped from Property24
File: Excel
Key Columns:
 - Price
 - Size (m²)
 - Bedrooms
 - Garages
 - Location

  **Data Cleaning**
  Removed "m²" and spaces from the Size coumn, converted to numeric.
  Converted Price to float
  Handled missing values:
    - Dropped rows with missing Size
    - Filled missing Garges with 0 (most likely apartments and don't have garages)
    - Filled missing Bedrooms with the median
    - Filled missing Bathrooms with the mode
  Created a clean version of Location called Location_Gouped by:
    - REmoving extensions like "Ext"
    - Consolidating variations of areas like "Bankenveld"
  Created Location_Score using median property prices by location

  **Exploratory Data Analysis & Visualisations**
  Distribution of prices (log scale histogram with KDE)
  Median Price By Location (all, top 10, bottom 10)
  Scatterplots:
    - Size vs Price
    - Bedrooms vs PRICE
    - Bathrooms vs Price
  Boxplot: Garages vs Price
  Correlation Heatmap: Among all numeric features

**Regression Model**
Features used:
- Bedrooms
- Bathrooms
- Garages
- Size
- Location_Score

Train/Test Split: 80% training, 20% tresting

Model used: Linear regression 

**Model Evaluation**
R² score: 0.0554
MAE: 469 338.73
