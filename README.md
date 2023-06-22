# Clinical Text Classification


This project focuses on classifying medical texts into different medical subspecialties using machine learning techniques. It involves preprocessing the data, extracting features, and training a classification model to predict the subspecialty of a given medical text.

#  Objectives:

2. Evaluate your model on each subspecialty of medicine
3. Code is modular and bug-free.
4. Use the following evaluation metrics (precision, recall, F1-score, support, macro avg, weighted avg, accuracy). Using more evaluation metrics is encouraged.
5. Spend time commenting and explaining your code.


# Requirements

Python 3.x
pandas
numpy
scikit-learn (sklearn)
Dataset

The project utilizes the mtsamples.csv dataset, which contains information about medical texts, including the transcription, medical specialty, and sample name. The dataset should be placed in the same directory as the project files.

# Setup

1. Install the required dependencies by running the following command:

```
  pip install pandas numpy scikit-learn
}
```
2. Clone the project repository from GitHub:
```
   git clone <repository_url>
```
3. Change to the project directory:
```
   cd medical-text-classification
```
5. Run the script:

# How it works

Data Preprocessing: The script loads the mtsamples.csv dataset and selects the relevant columns (transcription, medical_specialty, sample_name). Any rows with missing values are dropped.
Data Splitting: The dataset is split into training and testing sets using a 70:30 ratio (can be changed). The training set is used for model training and the testing set for evaluating the model's performance.
Feature Extraction: Text features are extracted using the TF-IDF (Term Frequency-Inverse Document Frequency) vectorizer. The training and testing data are transformed into vectorized representations.
Model Selection and Fine-tuning: The script uses a Multinomial Naive Bayes classifier to classify the medical subspecialties. A grid search is performed to find the best value for the hyperparameter alpha using 5-fold cross-validation.
Model Training and Evaluation: The best model obtained from the grid search is trained on the training data and evaluated on the testing data. The classification report, including precision, recall, and F1-score, is printed for the subspecialty classification using Multinomial Naive Bayes.

# Results

The script prints the classification report for the subspecialty of medicine using Multinomial Naive Bayes. The report includes metrics such as precision, recall, and F1-score for each class.

Example output:
```
Subspecialty of Medicine Classification Report using Multinomial Naive Bayes:
                            precision    recall  f1-score   support

                 Allergy / Immunology       1.00      0.95      0.98        37
                        Bariatrics       1.00      0.96      0.98        27
                      Cardiology         0.98      0.96      0.97       110
...

```

