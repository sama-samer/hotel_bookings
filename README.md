# hotel_bookings
# 🏨 Hotel Bookings Preprocessing

## Overview
The goal of this project is to clean and preprocess the **Hotel Bookings Dataset** to prepare it for a machine learning model predicting **last-minute booking cancellations**.

## Project Structure

hotel_bookings_project/
│
├── data/
│   ├── raw/
│   │   └── hotel_bookings.csv          # Original dataset
│   ├── processed/
│   │   ├── X_train.csv                 # Training features
│   │   ├── X_test.csv                  # Test features
│   │   ├── y_train.csv                 # Training target
│   │   └── y_test.csv                  # Test target
│
├── notebooks/
│   └── hotel_bookings_preprocessing.ipynb  # Jupyter Notebook with EDA & cleaning
│
├── src/
│   ├── data_cleaning.py                # Functions for handling missing values, duplicates
│   ├── feature_engineering.py          # Functions for feature creation & encoding
│   ├── outlier_detection.py            # Functions for IQR, boxplots, capping
│   └── utils.py                        # Helper functions
│
├── app.py                              # Optional Streamlit app for exploration
├── requirements.txt                    # Python dependencies
├── README.md                           # Project documentation
└── reports/
    ├── data_quality_report_phase1.csv  # Saved data quality report
    └── figures/                        # Plots and visualizations


## Phases
### Phase 1: Exploratory Data Analysis (EDA)
- Load dataset and explore structure  
- Check and visualize missing values  
- Detect outliers using boxplots and IQR  

### Phase 2: Data Cleaning
- Handle missing values (`company`, `agent`, `country`, `children`)  
- Remove duplicates  
- Cap extreme outliers (e.g., `adr > 1000`)  

### Phase 3: Feature Engineering
- Create new features: `total_guests`, `total_nights`, `is_family`  
- Remove data leakage columns  
- Encode categorical variables (one-hot & frequency encoding)  
- Split dataset into **Train/Test**  

---

## Tools & Libraries
- Python 3.10+  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn  
- Streamlit (optional, for interactive app)  

---

## Usage
Run preprocessing pipeline in Jupyter Notebook:
```bash
jupyter notebook hotel_bookings_preprocessing.ipynb
