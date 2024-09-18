# Inf-gram practical on ensemble learning

**Objective** : We are going to create a machine learning approach able to clasiify if a tumor is malignant or not taking into consideration differtent metrics of the tumor.

**Useful links:**

* Confusion matrix https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html
* AUC score https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_auc_score.html#sklearn.metrics.roc_auc_score
* SVM https://scikit-learn.org/stable/modules/svm.html
* Gridseach https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html
* Decision Trees https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html
* Randomforest https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
* Voting classifiers https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.VotingClassifier.html

# 1. Data set : Breast Cancer Wisconsin Data set

https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data


```python
import pandas as pd
import matplotlib.pyplot as plt

from sklearn.datasets import load_breast_cancer
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import MinMaxScaler
from sklearn.preprocessing import StandardScaler

from sklearn.ensemble import RandomForestClassifier
from sklearn.ensemble import VotingClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.svm import SVC

from sklearn.metrics import roc_auc_score
from sklearn.metrics import roc_curve
from sklearn.metrics import RocCurveDisplay
from sklearn.metrics import recall_score
from sklearn.metrics import confusion_matrix
from sklearn.metrics import ConfusionMatrixDisplay

SEED = 42

cancer = load_breast_cancer()
df =  pd.DataFrame(cancer.data, columns=[cancer.feature_names])
df['target'] = cancer.target
X = df.drop('target', axis=1)
y = cancer.target
```

**Discovring the data:**

1) Print the main charactersitics of the data set: Size, description, if it has null values, and show the first five rows and the statistical properties of each input feature.
2) Normalize the data
3) Split the dataset in train/test

**Machine leaning analysis:**

4) Implement a model of SVM, chose various kernels. Carry out grid search with random forest to calculate de best hyperparameters. Which one works better? Show the confusion matrix, the AUC, the precision and the recall for each type of kernel?
5) Is there overfitting? How can we check it ? 
6) Implement a decision tree based model. Do the same evaluation.
7) Repeat with a Randoml Forest model. Carry out grid search with random forest to calculate de best hyperparameters. what is the optimal number predictors? Check the importance of each feature in the clasification
8) Create a voting classifier taking as input the best model of each family. Do the performace evaluation and check for the overfitting.