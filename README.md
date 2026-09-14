# Supermarket Transaction Preprocessing & Customer Segmentation

## 1. Executive Summary
This project analyzes a 9,800-record retail transaction dataset to evaluate purchasing patterns, clean messy transaction metrics, and segment customer demand behavior for targeted retail operations.

## 2. Pipeline & Methodology
* **Data Cleansing:** Handled missing postal data via median imputation and verified zero duplicate records across 9,800 entries.
* **Feature Engineering:** Extracted temporal behavioral attributes including `Order Month` and `Ship Duration` (`Ship Date` - `Order Date`).
* **Outlier & Skewness Treatment:** Applied 1.5*IQR capping and square-root transformation on skewed `Sales` revenue distributions.
* **Encoding & Scaling:** Implemented one-hot encoding on categorical channels (`Ship Mode`, `Segment`, `Region`, `Category`) and target encoding for high-cardinality geographic features (`City`, `State`, `Sub-Category`), followed by `StandardScaler` normalization.
* **Clustering Analysis:** Evaluated cluster viability using the Elbow Method (WCSS) and applied K-Means clustering to identify distinct customer ordering behaviors.

## 3. Tech Stack
* Python, Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn[cite: 3]
