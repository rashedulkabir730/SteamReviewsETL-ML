
### Steam Reviews Analysis and Prediction

This project involves analyzing and building a predictive machine learning model on the Steam Reviews dataset, which contains over 100 million reviews for games on the Steam platform. The dataset is sourced from Kaggle and includes various features, such as review content, user playtime, votes, and whether the game was received for free.

#### Dataset Details
- **Source:** [Steam Reviews Dataset on Kaggle](https://www.kaggle.com/datasets/kieranpoc/steam-reviews)

#### Objective
To develop a machine learning model that predicts whether a review has a weighted score greater than 0.4. The label is binary, where:
- `1`: Weighted score ≤ 0.4
- `0`: Weighted score > 0.4

#### Process
1. **Data Pipeline and ETL:**
   - Data extracted and processed using PySpark on Google Cloud Platform.
   - Non-English reviews and irrelevant columns filtered out.
   - Timestamp errors corrected and NaN values addressed.
   - Feature engineering included:
     - Tokenization and TF-IDF transformation of reviews.
     - One-hot encoding of categorical variables.
     - Scaling of numerical features.
   - Final features assembled into a single vector for modeling.

2. **Modeling:**
   - Logistic regression was used for binary classification.
   - Achieved an accuracy of **65%** on the full dataset.
   - Hyperparameter tuning (grid search with cross-validation) did not improve accuracy.
   - Model performance evaluated using confusion matrix, ROC curve, and feature importance analysis.

3. **Visualization:**
   - Exploratory plots, including review word counts, votes correlation, and feature importance.
   - Confusion matrix and ROC curve provided insights into model performance.

#### Key Findings
- Majority of reviews are in English, accounting for approximately 20GB of the data.
- Features like `voted_up` and `received_for_free` had the highest impact on predictions.
- Potential improvements include refining features further and experimenting with advanced models.

#### Conclusion
This project demonstrated a complete pipeline for large-scale data processing and machine learning model building. The model provides a framework for identifying reviews that may not benefit prospective game buyers, such as nonsensical or irrelevant content, ensuring meaningful and helpful reviews are highlighted.


