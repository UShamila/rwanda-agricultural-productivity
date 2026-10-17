# Predicting Agricultural Productivity Levels in Rwanda

## About the Project

This project uses data from the Rwanda Seasonal Agricultural Survey (SAS) 2025, Season A, to classify agricultural records into three productivity groups: **Low, Medium, and High**.

The project compares traditional machine learning models and neural networks to explore how selected crop, location, farmer, and land-area characteristics can help classify agricultural productivity.

## Objectives

- Explore and prepare the agricultural survey data.
- Create productivity classes using crop yield values.
- Train and compare traditional machine learning and deep learning models.
- Evaluate model performance using classification metrics and visualizations.

## Dataset

The project uses the Season A Production file from the Rwanda Seasonal Agricultural Survey 2025, published by the National Institute of Statistics of Rwanda (NISR).

- Original dataset: 34,369 records
- Records retained after cleaning: 29,938
- Target variable: `productivity_class`
- Classes: Low, Medium, and High

The productivity classes were created using the 33rd and 67th percentiles of yield. These are project-defined categories and are **not official NISR productivity classifications**.

The original dataset is not included in this repository. Anyone wishing to use the data should follow NISR's access and sharing conditions.

## Models

The project evaluates the following models:

- Logistic Regression
- Random Forest
- Gradient Boosting
- Tuned Random Forest
- Neural Network 1
- Neural Network 2

The neural networks were developed using TensorFlow/Keras. The traditional machine learning models and preprocessing steps were implemented using scikit-learn.

## Results

Neural Network 2 achieved the best overall results in the project:

- **Test accuracy:** 80.36%
- **Macro F1-score:** 0.8003
- **Macro ROC-AUC:** 0.9327

The tuned Random Forest performed closely, achieving 80.14% test accuracy and a macro F1-score of 0.7984.

The Medium productivity class was more difficult to classify than the High class. The results suggest that the selected variables contain useful patterns, but the model should not be used as the only basis for agricultural decisions.

## Project Files

The repository may contain:

- `Agricultural_Productivity_Classification.ipynb` — the notebook containing data preparation, model training, evaluation, and visualizations.
- `requirements.txt` — the Python libraries needed to run the notebook.


## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries:

   ```bash
   pip install -r requirements.txt
   ```

3. Obtain the SAS 2025 Season A dataset according to NISR's access conditions.
4. Upload or place the dataset ZIP file where the notebook expects it.
5. Open the notebook in Jupyter Notebook or Google Colab.
6. Run the notebook cells in order.

Some file-loading steps may need to be adjusted depending on where the dataset is stored.

## Limitations

- The analysis uses Season A 2025 data only.
- The productivity classes are based on the yield distribution in this dataset.
- The models use a selected set of features rather than all available survey variables.
- The results show patterns in the data but do not prove that a particular factor causes higher productivity.

Future work could test the models on data from other seasons and investigate additional agricultural variables.

## Author

**Shamila UWINEZA**

