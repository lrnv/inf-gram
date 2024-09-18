# Inf-gram Practical 3: Ensemble Learning

**Objective:** Create machine leaning approaches to classify a tumor as malignant or not, taking different metrics of the tumor in consideration.

**Useful links:**
* Confusion matrix https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html
* AUC score https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_auc_score.html#sklearn.metrics.roc_auc_score
* SVM https://scikit-learn.org/stable/modules/svm.html
* Gridseach https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html
* Decision Trees https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html
* Randomforest https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html
* Voting classifiers https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.VotingClassifier.html

**Data set : Breast Cancer Wisconsin Data set**

The dataset can be found here: https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data
The following python code loads it: 

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

**Tasks:**
1. Discovering the data
    a. Print the main charactersitics of the data set: size, description, if it has null values, and show the first five rows and the statistical properties of each input feature.
    b. Normalize the data
    c. Split the dataset in train/test
2. Machine learning analysis: SVM
    a. Implement a SVM, chose various kernels. 
    b. Carry out grid search with random forest to calculate de best hyperparameters. Which one works better? 
    c. Show the confusion matrix, the AUC, the precision and the recall for each type of kernel.
    d. Is there overfitting? How can we check it ? 
3. Same question for a decision tree
4. Same question for a Random forest. 
    a. What is the optimal number of predictors?
    b. Check the feature importances in the classification.
5. Ensemble learning
    a. Create a voting classifier taking as input the best model of each family. 
    b. Do the performace evaluation and check for the overfitting.

**Submission:** Submit your notebook in full (e.g., the collab file), including comments and responses to the questions.