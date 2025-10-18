
# Global Earthquake-Tsunami Risk Analysis and Prediction

## Project Overview

This project utilizes advanced machine learning techniques to analyze and predict the global risk of an earthquake generating a tsunami. Using historical seismic data, the goal is to develop a robust binary classification model that can distinguish between tsunami and non-tsunami-generating earthquakes, which is critical for early warning systems and disaster mitigation.

The analysis includes comprehensive Exploratory Data Analysis (EDA), statistical testing to uncover key feature relationships, and the development and evaluation of multiple classification models.

## Key Findings & Results

### Exploratory Data Analysis (EDA)
* **Data Size:** The analysis was conducted on a dataset of 782 global earthquake events.
* **Tsunami Rate:** Approximately **38.87%** of the recorded events generated a tsunami.
* **Event Averages:** Tsunami events had a mean magnitude of **6.94** and a mean depth of **85.66 km**.

### Statistical Testing
* The **Mann-Whitney U Test** was used to compare the distribution of key features (`magnitude` and `depth`) between the tsunami (1) and non-tsunami (0) groups.
* The tests concluded that there was **no significant difference** found in the distribution of magnitudes or depths between the two groups (p-values > 0.05). This confirms that a direct threshold for these individual features is insufficient for reliable prediction, necessitating a complex machine learning approach.

### Machine Learning Model Performance

After evaluating several models, the **Gradient Boosting Classifier** was selected as the best-performing model based on the F1 Score for the minority class (tsunami).

| Metric | Chosen Model: Gradient Boosting |
| :--- | :--- |
| **AUC Score** | 0.7297|
| **Tsunami F1 Score** | **0.5612**|
| **Tsunami Recall** | 0.5132|

## Technologies Used

* **Python**
* **pandas** (Data manipulation)
* **numpy** (Numerical operations)
* **matplotlib** & **seaborn** (Visualization)
* **scipy** (Statistical testing - Mann-Whitney U Test)
* **scikit-learn** (Machine Learning models - Gradient Boosting) (Inferred from project description and notebook execution)

## Installation and Setup

1.  **Clone the repository:**
    ```bash
    git clone [YOUR-REPO-LINK]
    cd global-earthquake-tsunami-risk
    ```

2.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn scipy
    ```

3.  **Run the analysis:**
    Open the Jupyter Notebook and run the cells sequentially.
    ```bash
    jupyter notebook "Global Earthquake-Tsunami Risk .ipynb"
    ```
