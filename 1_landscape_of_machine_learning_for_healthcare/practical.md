# INF-GRAM — Practical 1: Critical reading of a machine-learning study

## Objective

The purpose of this practical is to learn how to **read a machine-learning paper critically**,
not simply to summarize it.

Choose one recent peer-reviewed article (published in 2021 or later) that uses machine learning
for a healthcare prediction, diagnosis, prognosis, phenotyping or risk-stratification problem.

PubMed should be your primary search tool. Google Scholar may be used to identify related work,
but the selected article must be accessible and scientifically citable. Example of a relevant article: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8234681/.

## Deliverables

Prepare a **7 to 8 minute presentation** followed by a few questions.

Your slides should answer the following questions.

### 1. Clinical question

- What is the population?
- What is the clinical task?
- What is the prediction or analysis target?
- At what point in the care pathway would the model be used?

### 2. Data

- How many patients / observations are included?
- Which sites and time period are represented?
- What are the predictors?
- How is the target or reference standard defined?
- Are missing data discussed?
- Is the sample representative of the intended population?

### 3. Machine-learning workflow

- Which model(s) are used?
- How are train, validation and test data separated?
- Is preprocessing fitted only on development data?
- How are hyperparameters selected?
- Is there any obvious risk of data leakage?

### 4. Evaluation

- Which performance metrics are reported?
- Are the chosen metrics appropriate for the clinical question?
- Are confidence intervals or uncertainty reported?
- Is calibration assessed when predicted probabilities are used?
- Is there external or temporal validation?

### 5. Interpretation

- What are the main results?
- What is one strength of the study?
- What is one important limitation?
- What would be required before clinical deployment?

## Submission

Submit your presentation as a PDF on Amétice before the deadline.


## Evaluation

The presentation will be assessed on:

- understanding of the clinical question;
- understanding of the validation strategy;
- interpretation of performance metrics;
- ability to identify limitations;
- clarity of the oral presentation.
