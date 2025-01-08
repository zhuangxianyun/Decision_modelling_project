# Decision Modeling Project: Nutri-Score Label Classification

## Overview
This repository contains the implementation of a food classification project based on the Nutri-Score system. The project explores various decision modeling techniques, including Multi-Criteria Decision Analysis (MCDA) methods and machine learning models, to classify food products into predefined categories based on their nutritional properties.

---

## Repository Structure

### Root Directory
- **`build_database.ipynb`**: Jupyter Notebook for building the initial dataset by integrating data from various sources and preprocessing.
- **`NutriScore_Presentation.pdf`**: Presentation slides summarizing the project and its findings.
- **`Project_Nutriscore_Label_2024_2025.pdf`**: Comprehensive project report detailing methodologies, analyses, and results.
- **`README.md`**: This documentation file providing an overview of the repository and usage instructions.

### `data/` Directory
Contains processed and intermediate datasets used in the project:
- **`food_data_classified.xlsx`**: Dataset with food items classified based on Nutri-Score and MCDA results.
- **`food_data_combined_mcda.xlsx`**: Dataset combining Nutri-Score, Eco-Score, and MCDA model results.
- **`food_data_cleaned1.xlsx`**: Cleaned dataset after handling missing values and duplicates.
- **`food_data_filtered.xlsx`**: Dataset filtered for relevant categories and features.

### `Decision Models/` Directory
Contains implementation and results of different decision models:
- **`dm_Electre-Tri.ipynb`**: Jupyter Notebook implementing the ELECTRE-Tri MCDA model for classification.
- **`dm_ml_model.ipynb`**: Notebook implementing machine learning models (Random Forest, KNN, Gaussian Naive Bayes, XGBoost).
- **`dm_Weighted_Sum_model_Rule_Model.ipynb`**: Notebook comparing the Weighted Sum and Simple Decision Rules models.
- **`electri_model.ipynb`**: Additional exploration and visualization for the ELECTRE-Tri model.
- **`Optimistic_Sorting.xlsx`**: Results of the optimistic ELECTRE-Tri sorting.
- **`Pessimistic_Sorting.xlsx`**: Results of the pessimistic ELECTRE-Tri sorting.
- **`weighted_sum_model_results.csv`**: Classification results using the Weighted Sum Model.
- **`weighted_sum_scaled_results.csv`**: Normalized results from the Weighted Sum Model.

---

## Methodology

### Data Processing
1. **Dataset Creation**:
   - Extracted data from the Open Food Facts API for categories like snacks, cereals, and beverages.
   - Preprocessed data by handling missing values, removing duplicates, and filtering for relevant features.
   
2. **Exploratory Data Analysis**:
   - Visualized ingredient distributions using bar charts, scatter plots, and box plots.
   - Examined correlations between key attributes (e.g., sugar, protein, energy).

### Decision Models
1. **ELECTRE-Tri Model**:
   - Sorted food products into categories based on threshold profiles and weights.
   - Compared pessimistic and optimistic versions under various lambda thresholds.

2. **Weighted Sum Model**:
   - Aggregated normalized Nutri-Score and Eco-Score values with weighted criteria.
   - Categorized food products into classes (A-E) based on aggregated scores.

3. **Simple Decision Rules Model**:
   - Used Nutri-Score as the primary classification criterion.
   - Incorporated Eco-Score as a secondary adjustment factor.

### Machine Learning Models
- Implemented Random Forest, KNN, Gaussian Naive Bayes, and XGBoost models.
- Evaluated performance based on accuracy, precision, recall, and F1-score.
- Compared results with MCDA models.

---

## Results
- **Random Forest** achieved the highest accuracy at 68.99%, followed by XGBoost.
- **ELECTRE-Tri** provided interpretable categorization but lagged in accuracy compared to machine learning models.
- **Simple Decision Rules** balanced interpretability and accuracy by integrating Nutri-Score and Eco-Score.
- All results are documented in the corresponding Notebooks and datasets.

---

## Usage

### Prerequisites
Ensure you have the following installed:
- Python 3.x
- Jupyter Notebook
- Required Python libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`

### Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/zhuangxianyun/Decision_modelling_project.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Decision_modelling_project
   ```

3. Run the Jupyter Notebooks in the following order:
   - `build_database.ipynb` to preprocess and generate the dataset.
   - `dm_Weighted_Sum_model_Rule_Model.ipynb` to apply and compare MCDA models.
   - `dm_ml_model.ipynb` to train and evaluate machine learning models.
   - `dm_Electre-Tri.ipynb` for ELECTRE-Tri model exploration.

4. Analyze the results stored in the `data/` and `Decision Models/` directories.

---

## References
- Nutri-Score Labeling: [https://ec.europa.eu](https://ec.europa.eu)
- Open Food Facts API: [https://world.openfoodfacts.org](https://world.openfoodfacts.org)
- ELECTRE-Tri Model: [Roy 2002, Cailloux 2012]

---

## Contributors
- **Jintao Ma**
- **Xianyun Zhuang**
- **Yutao Chen**

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.
