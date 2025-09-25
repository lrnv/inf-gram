# Inf-Gram final project. 

**Objectives:**
1. Import and process an unknown dataset
2. Do some descriptive analysis of the data
3. Compute different classification model
4. Evaluate the models and select the final model


**Context:** For this project, we will be working on biomedical data related to vertebral column conditions. In particular, _disk-hernia_ and _spondylolisthesis_. The first one, _disk-hernia_, is a condition in which the annulus fibrosus (outer portion) of the vertebral disc is torn, enabling the nucleus (inner portion) to herniate or extrude through the fibers. The herniated material can compress the nerves around the disc and create pain that can radiate through the back and sometimes down the arms (if the herniation is in the cervical spine) and legs (if the herniation is in the lumbar spine). The second condition, _spondylolisthesis_ is a slipping of vertebra that occurs, in most cases, at the base of the spine. The extent of slippage determines the grade of _sponylolisthesis_. The two conditions can be diagnosed visually via physical exam, X-ray, MRI and radiology technologies.

**Data:** The dataset `column_3C` has 310 instances of patients data. Each patient is represented in the dataset by six bio-mechanical attributes derived from the shape and orientation of the pelvis and lumbar spine:

* `pelvic incidence:` pelvic tilt + sacral slope
* `pelvic tilt:` is the angle between  a vertical line and the CS segment. Denotes spatial orientation of pelvis.
* `lumbar lordosis angle`
* `sacral slope` The sacral slope is the angle of the sacral plateau to the horizontal. The degree of the sacral slope determines the position of the lumbar spine, since the sacral plateau forms the bae of the spine
* `pelvic radius`
* `degree_spondylolisthesis:` degree of severity of spondylolisthesis. Grade 1 being least severe through to grade 4 most severe.
* `class:` Disk Hernia (DH), Spondylolisthesis (SL), Normal (NO)

**Expected work:** For this project, you will use the 6 variables to classify the patients. The target variable is `class`. The project consist in building different models from the dataset, evaluate them with different indicators, consider calibration of hyper-parameters and finally decide which model you would keep. You can find the dataset on the Ametice webpage or [at this link](https://github.com/lrnv/inf-gram/blob/main/6_final_project/column_3C.txt).

**Task 1:** Import and pre-process the dataset

1. Set-up your environment by importing the libraries that you will need for the rest of the project.
2. Import the dataset `column_3C.txt` and do the following checking
    a. Display the first lines
    b. Display the number of rows and columns
    c. Check the data type (all features are supposed to be numeric except class)
    d. Check if there is any missing value
    e. Give the number of patients/rows in each class of the dataset

We will now work with 2 classes instead of 3. The new classes will be:
- Normal (NO)
- Abnormal (AB) = {Disk Hernia, Spondylolisthesis}. 

3. Generate the new class feature. Display the new repartition of the two classes (e.g., as a table or with a graph).

**Task 2:** Univariate descriptive analysis

4. Compute and display the mean and standard deviation values of each feature.
5. Compute and display the mean and standard deviation values for each feature in each class (Normal and Abnormal).
6. Give the distribution of each feature and for each class in a graphic (use two histograms, on for each class, in a single plot).
7. Compute the correlation matrix. Make some comments about the correlation of the features.
8. Split the dataset in two parts, a training sample and a test sample (with 80% of the data in the training sample.)

**Task 3:** Logistic regression

8. Build the logistic model for the classification, and compute your prediction on the test sample
9. Compute and display the confusion matrix for the test sample
10. Choose some performance indicators to compute from the confusion matrix and present them for the logistic regression.

**Task 4:** Another model of your choice

For the task 4 and 5 you have more freedom to choose which model you want to test. But whatever the model you will have to take into account the following things:

11. Give a justification of your choice
12. Use the same train sample as Task 3 to build the model.
13. For each model, use the same performance indicators and display the confusion matrix for the test sample.
14. If there's any parameters to calibrate, first do the default model first (without calibration) and then do your calibration, compare the performances of the calibrated model and the default one on the test sample.

**Task 5:** Third model

For the task 4 and 5 you have more freedom to choose which model you want to test. But whatever the model you will have to take into account the following things:

15. Give a justification of your choice
16. Use the same train sample as Task 3 to build the model.
17. For each model, use the same performance indicators and display the confusion matrix for the test sample.
18. If there's any parameters to calibrate, first do the default model first (without calibration) and then do your calibration, compare the performances of the calibrated model and the default one on the test sample.

**Task 6** Comparison of the model and final model

19. For the last task, use a table to present the performance of the three model on the test sample. 
20. Choose a final model and argument your choice.

**Submission:** You should submit the collab notebook with all the codes, graphs, comments and answers to the questions. 

**Evaluation:** At the oral examination, you will be asked to execute the project in live and comment on the main results. We will ask questions about the results and technical developepments. The total oral duration will be about 15 minuts.