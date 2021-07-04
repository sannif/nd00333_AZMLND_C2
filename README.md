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

### Swagger Documentation
We consume the deployed model using Swagger. We download the [swagger.json](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/starter_files/swagger/swagger.json) file of the deployed model and using the bash script [swagger.sh](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/starter_files/swagger/swagger.sh) and the Python script [server.py](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/starter_files/swagger/serve.py) to consume the model.

**Swagger screenshot**
![swagger1](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/images/swagger1.PNG)
![swagger2](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/images/swagger2.PNG)

### Consume model endpoint
Here we consume the model endpoint by executing the script the [endpoint.py](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/starter_files/endpoint.py) against the model API. Below is the *Json* output from the model.  
![endpoint](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/images/endpoint.PNG)

**Benchmark**  
Using the Apache Benchmark command-line tool, we test the performance of our model.  
![benchmark](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/images/bench1.PNG)
![benchmark2](https://github.com/sannif/nd00333_AZMLND_C2/blob/0bc031199a3d5abe84c3481f35c2eab3660da4e5/images/bench2.PNG)

### Pipeline
We use the jupyter notebook [notebook](https://github.com/sannif/nd00333_AZMLND_C2/blob/master/starter_files/aml-pipelines-with-automated-machine-learning-step.ipynb) to create a pipeline.  
**Pipeline creation**  
![pipeline_creation](https://github.com/sannif/nd00333_AZMLND_C2/blob/9ffcdd9ebb23ee390aa5d28dd1e0c9be233a57de/images/pipeline.PNG)

**Pipeline endpoint**  
![pipe_endpoint](https://github.com/sannif/nd00333_AZMLND_C2/blob/9ffcdd9ebb23ee390aa5d28dd1e0c9be233a57de/images/pipeline_endpoint.PNG)

**Published pipeline overview**  
The pipeline is *Active* with a REST endpoint.
![published_pipeline](https://github.com/sannif/nd00333_AZMLND_C2/blob/9ffcdd9ebb23ee390aa5d28dd1e0c9be233a57de/images/pipeline_active.PNG)

**Run details from Jupyter Notebook**  
Below is the screenshot of the run details showing the run steps.  
![run_details](https://github.com/sannif/nd00333_AZMLND_C2/blob/9ffcdd9ebb23ee390aa5d28dd1e0c9be233a57de/images/run_details.PNG)

**Scheduled run**  
We do a request to the pipeline endpoint to trigger a run.  
![schedule_run](https://github.com/sannif/nd00333_AZMLND_C2/blob/9ffcdd9ebb23ee390aa5d28dd1e0c9be233a57de/images/pipeline_scheduled_run.PNG)

## Screencast
We did a screencast of Azure ML Studio that shows the entire process of the working ML application, including a demonstration of:  
* Working deployed ML model endpoint.
* Deployed Pipeline
* Available AutoML Model
* Successful API requests to the endpoint with a JSON payload  

The screencast is available [here](https://youtu.be/BI4JYFJBqhk).
