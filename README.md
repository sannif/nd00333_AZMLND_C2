# Operationalizing Machine Learning

## Overview
This project is part of the Udacity Azure ML Nanodegree. In this project, we build, deploy, and consume a model using Azure AutoML on the [Bank Marketing dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing). We also create, publish, and consume a pipeline.

## Architectural diagram

## Steps
### AutoML Experiment
We run an AutoML experiment on the Bankmarketing dataset and select the best model.

**Bankmarketing Data set in ML Studio**  
We upload the Bankmarketing dataset to ML Studio.
![Bankmarketing Data set in ML Studio](https://github.com/sannif/nd00333_AZMLND_C2/blob/d5168e72736c8c7d2c055a9742a3f7a2c2b55c47/images/dataset1.PNG)

**AutoML Experiment run**  
The AutoML ran for 20 minutes successfully.
![AutoML Experiment run](https://github.com/sannif/nd00333_AZMLND_C2/blob/9d61ce02d3376d294ec69b7d575119203d1b9014/images/automl_run.PNG)

**AutoML Experiment run - Details**
![AutoML Experiment run - Details](https://github.com/sannif/nd00333_AZMLND_C2/blob/9d61ce02d3376d294ec69b7d575119203d1b9014/images/automl_run2.PNG)

**Best Model**  
The best model is an *XGBoost Classifier** with a *SparseNormalizer* processing.
![best model](https://github.com/sannif/nd00333_AZMLND_C2/blob/472f472549716c3ab5c017db923c19caf1ab9722/images/best_model.PNG)

### Best model deployment
We deploy the best model using Azure Container Instance. We also enable authentication.

### Application Insights
We enable applications insights on the deployed model.  
**Insights enabled**
![](https://github.com/sannif/nd00333_AZMLND_C2/blob/472f472549716c3ab5c017db923c19caf1ab9722/images/insights_enabled.PNG)

**Logs**  
We run the scripts [logs.py](https://github.com/sannif/nd00333_AZMLND_C2/blob/472f472549716c3ab5c017db923c19caf1ab9722/starter_files/logs.py) to retrieve some logs.
![logs](https://github.com/sannif/nd00333_AZMLND_C2/blob/472f472549716c3ab5c017db923c19caf1ab9722/images/logs.PNG)
