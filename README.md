# Exoplanet Classification using XGBoost

This project utilizes machine learning to classify Exoplanet candidates identified by the Kepler Space Telescope. Using the XGBoost classifier, the model predicts whether a Kepler Object of Interest (KOI) is a "CONFIRMED" exoplanet, a "CANDIDATE", or a "FALSE POSITIVE" based on various astrophysical features.

##  Project Overview

The primary objective of this notebook is to build a robust classification model capable of distinguishing between real exoplanets and false positives. The project involves:
* **Data Loading & Cleaning**: Handling the Kepler dataset.
* **Exploratory Data Analysis (EDA)**: Visualizing distributions of orbital periods, planet radii, and equilibrium temperatures.
* **Feature Engineering**: Preparing features for the model.
* **Model Training**: Implementing an XGBoost Classifier.
* **Evaluation**: Assessing performance using classification reports and confusion matrices.

##  Dataset

The dataset used is `kepler_data.csv`. It contains data collected by the Kepler Space Telescope, including properties such as:
* `koi_disposition`: The target label (CONFIRMED, CANDIDATE, FALSE POSITIVE).
* `koi_period`: Orbital period of the candidate.
* `koi_prad`: Planetary radius.
* `koi_teq`: Equilibrium temperature.
* `koi_insol`: Insolation flux.
* And various error measurements and flags for false positive detection.

##  Technologies & Libraries

The analysis is performed using Python with the following major libraries:

* **Pandas** & **NumPy**: Data manipulation and numerical operations.
* **Matplotlib** & **Seaborn**: Data visualization (histograms, count plots, heatmaps).
* **Scikit-Learn**: Model selection (`train_test_split`), metrics (`classification_report`, `confusion_matrix`), and preprocessing.
* **XGBoost**: Gradient boosting framework for the classification model.
* **IsolationForest**: Used for outlier detection.

##  Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/yourusername/exoplanet-classification.git](https://github.com/yourusername/exoplanet-classification.git)
    cd exoplanet-classification
    ```

2.  **Install dependencies:**
    Ensure you have Python installed, then install the required packages:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn xgboost
    ```

3.  **Run the Notebook:**
    Launch Jupyter Notebook or Jupyter Lab and open the file:
    ```bash
    jupyter notebook "Exoplanet_Classification_(xgboost).ipynb"
    ```

##  Methodology

1.  **Data Ingestion**: The data is loaded using Pandas, filtering out comment lines.
2.  **EDA**: 
    * Class balance check using count plots (`koi_disposition`).
    * Feature distribution histograms for key metrics like orbital period and radius.
3.  **Preprocessing**: Handling missing values and encoding categorical labels.
4.  **Modeling**: 
    * Splitting data into training and testing sets.
    * Training an **XGBoost Classifier**.
5.  **Evaluation**: The model's performance is evaluated using precision, recall, F1-score, and accuracy metrics.

##  Results

* The dataset typically shows a class imbalance, with a high number of "FALSE POSITIVE" results compared to "CONFIRMED" planets.
* The XGBoost model provides feature importance scores, highlighting which physical properties (like orbital period or impact parameter) are most critical for classification.

##  Contributing

Contributions, issues, and feature requests are welcome! Feel free to fork this repository and submit pull requests.

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
