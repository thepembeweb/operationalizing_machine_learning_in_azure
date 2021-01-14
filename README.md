# Operationalizing Machine Learning pipeline in Azure

This project demonstrates how to use Azure to configure a cloud-based machine learning production model, deploy it, and consume it. IN addition it involves how to create, publish, and consume a pipeline.

## Architectural Diagram
![alt Architectural Diagram](screenshots/ml-architecture.png)

1. **Authentication** : In this step, we need to create a Security Principal (SP) to interact with the Azure Workspace.
2. **Automated ML Experiment** : In this step, we create an experiment using Automated ML, configure a compute cluster, and use that cluster to run the experiment.
3. **Deploy the best model** : Deploying the Best Model will allow us to interact with the HTTP API service and interact with the model by sending data over POST requests.
4. **Enable logging** : Logging helps monitor our deployed model. It helps us know the number of requests it gets, the time each request takes, etc.
5. **Swagger Documentation** : In this step, we consume the deployed model using Swagger.
6. **Consume model endpoints** : We interact with the endpoint using some test data to get inference.
7. **Create and publish a pipeline** : In this step, we automate this workflow by creating a pipeline with the Python SDK. 

## Key Steps

### 1: Authentication
Authentication was done through the provided Udacity lab. 

### 2: Automated ML Experiment

  * Create a New Automated ML run
  * Select and upload the Bankmarketing dataset
   ![alt Architectural Diagram](screenshots/1-registered-datasets.png)
  * Configure a new compute cluster with **Standard_DS12_v2** for the Virtual Machine Size and **1** as the number of minimum nodes.
  * Run the experiment using **Classification**, ensure **Explain best model** is checked. <br> On Exit criterion, reduce the default (3 hours) to 1 and reduce the             **Concurrency** from default to 5 (this number should always be less than the number of the compute cluster)
  * Experiment completed
    ![alt Experiment completed](screenshots/2-experiment-completed.png)
  * Best model after experiment completed
    ![alt Best model after experiment completed](screenshots/3-best-model-after-experiment-completed.png)

### 3: Deploy the best model

### 4: Enable logging

### 5: Swagger Documentation

### 6: Consume model endpoints

### 7: Create and publish a pipeline

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
