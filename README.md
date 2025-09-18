# Bengaluru House Price Prediction

A machine learning project that predicts house prices in Bengaluru using linear regression with comprehensive data preprocessing and feature engineering.

## 📋 Project Overview

This project analyzes and predicts house prices in Bengaluru based on various features like location, size, area type, availability, and amenities. The model uses linear regression with extensive data preprocessing to achieve accurate price predictions.

## 🎯 Objectives

- Predict house prices in Bengaluru based on property features
- Perform comprehensive data cleaning and preprocessing
- Handle categorical variables through encoding techniques
- Remove outliers to improve model performance
- Compare different data scaling and encoding approaches

## 📊 Dataset

The dataset contains **13,320 house records** from Bengaluru with the following features:

- **area_type**: Type of area (Super built-up, Built-up, Plot, Carpet)
- **availability**: Property availability status
- **location**: Property location in Bengaluru
- **size**: Number of bedrooms (BHK)
- **society**: Housing society name
- **total_sqft**: Total square footage
- **bath**: Number of bathrooms
- **balcony**: Number of balconies
- **price**: Property price in lakhs (target variable)

## 🔧 Key Features

### Data Preprocessing
- **Missing Value Treatment**: Handled 5,502 missing society values by dropping the column
- **Data Type Conversion**: Converted size from categorical to numerical
- **Range Handling**: Processed total_sqft ranges (e.g., "2100-2400") by taking averages
- **Unit Standardization**: Handled different area units (Sq. Meter, Sq. Yards, etc.)

### Feature Engineering
- **Location Consolidation**: Reduced 1,300+ locations to top 100 locations (≥30 properties)
- **Categorical Encoding**: Applied both label encoding and binary encoding
- **Outlier Detection**: Used statistical methods (mean ± 2σ) for outlier removal
- **Price Per Square Foot**: Created PPS feature for outlier detection

### Data Cleaning Pipeline
1. **Size Standardization**: Converted "2 BHK", "3 BHK" to numerical values
2. **Area Type Simplification**: Reduced to "Super built-up Area" vs "Other Area Type"
3. **Availability Grouping**: Simplified to "Ready To Move" vs "Under Construction"
4. **Location Normalization**: Handled spelling variations and consolidated similar locations
5. **Zero Value Imputation**: Filled missing bathrooms and balconies based on property size

## 🚀 Installation & Usage

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
