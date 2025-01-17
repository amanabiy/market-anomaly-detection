# Anomaly Detection Project

This project focuses on detecting anomalies in the market before they occur using a machine learning model trained on historical anomaly data. Below is an overview of the approach, data, methodologies, and results.

## Table of Contents
1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Methodology](#methodology)
4. [Models and Performance](#models-and-performance)
5. [Feature Engineering](#feature-engineering)
6. [Results](#results)
7. [How to Use](#how-to-use)
8. [Future Improvements](#future-improvements)
9. [Contributing](#contributing)
10. [Acknowledgments](#acknowledgments)

---

## Introduction
This project uses a machine learning approach to predict whether a market anomaly is happening or not, based on historical market data. The objective is to identify patterns in past anomalies and leverage this information to anticipate future anomalies.

---

## Dataset
The dataset is found on the file `anomaly_detection.csv`

### Data Preprocessing
- Cleaned the raw data for missing or inconsistent entries.
- Explored the distribution of anomalies and normal instances.
- Visualized the frequency and patterns of anomalies over time.

---

## Methodology
1. **Data Cleaning**: Removed noise and inconsistencies.
2. **Exploratory Data Analysis (EDA)**:
   - Analyzed distributions of anomalies vs. normal data points.
   - Visualized anomaly trends over time.
3. **Feature Engineering**:
   - Added lagged features for time-series context.
   - Computed **Relative Strength Index (RSI)** for performance enhancement.
4. **Model Selection**:
   - Trained **Random Forest** and **XGBoost** models.
   - Evaluated performance metrics: Precision, Recall, and F1-score.
5. **Dimensionality Reduction**:
   - Applied **Principal Component Analysis (PCA)** to improve model performance.
6. **Hyperparameter Optimization**:
   - Used Grid Search for tuning hyperparameters.

---

## Models and Performance
### Models Trained
1. **Random Forest**: 
   - Good performance on normal instances but struggled with anomalies.
2. **XGBoost**:
   - Achieved better recall for anomalies but required further tuning for balanced precision and recall.

### Dimensionality Reduction
- PCA improved precision and recall for XGBoost, making it the selected model.
- Correlation analysis had limited impact compared to PCA.

### Final Model
The **XGBoost model with PCA** was selected for deployment, balancing precision and recall effectively.

---

## Feature Engineering
- **Lag Features**: Incorporated time-series lags for better anomaly detection.
- **RSI Calculation**: Enhanced the model's ability to recognize shifts in stock trends.

---

## Results
- **XGBoost with PCA** showed the best balance of precision and recall for anomalies.
- Model metrics:
  - **Precision**: Higher for normal instances.
  - **Recall**: Improved significantly for anomalies post-PCA.

---

## How to Use
1. **Set Up a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Train the Model**:
   run all for the anomaly_detection.ipynb book.

---

## Future Improvements
- Improve anomaly detection precision by further refining features.
- Experiment with additional models like neural networks.
- Investigate alternative dimensionality reduction techniques.
- Collect more diverse and granular data for improved generalization.

---

## Contributing
Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.

---

## Acknowledgments
Thank you to everyone who provided feedback and support for this project. Your insights have been invaluable.

---

Feel free to reach out if you have any questions or suggestions!