# Project Overview:

This project explores building and deploying a machine learning model for a bank marketing scenario. We'll leverage Azure's cloud capabilities to achieve the following:

Model Training:
Utilize Azure AutoML for automated model building with a classification task.
Deploy the highest-performing model (a voting ensemble in this case).
Model Deployment:
Host the model on Azure Container Instances (ACI) with secure authentication.
Expose the model through REST endpoints for easy access.
Pipeline Creation:
Design and publish a machine learning pipeline using Azure ML Studio or Python SDK.
Enable consumption of the pipeline through REST endpoints.

## Architectural Diagram

![Architectural Diagram](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/421bd1a00ed9547d00b5d4a0fbd18cef736526f4/screenshots/Architecture%20Diagram.jpeg)

## Key Steps

1. Authentication
Authentication is an essential aspect of ensuring that operations run smoothly. Continuous Integration and Delivery (CI/CD) systems rely on uninterrupted flows. When authentication is not set up correctly, it requires human intervention, which can interrupt the flow. Ideally, the system should not stop waiting for a user to input a password. Therefore, it’s advisable to use automation for authentication whenever possible. There are three types of authentication: Key-Based, Token-Based, and Interactive.

Udacity Classroom - "If you are using the lab Udacity provided to you, you can skip this step since you are not authorized to create a security principal".So, this step is skipped in Azure.

2. Automated ML Experiment

My workspace: 
![My workspace](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/1.workspace.jpg)

Dataset snapshot that I am using: 
![Data](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/2.data.jpg)

Selecting task as Classification and selecting data for modelling: 
![task type selection](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/3.task%20type%20selection.jpg)

Creating compute cluster:
![creating compute cluster](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/4.creating%20compute%20cluster.jpg)

Running the automl model:
![automl model running](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/5.automl%20model%20running.jpg)

AutoML model training completion:
![automl model completed](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/6.automl%20model%20completed.jpg)

Model Details are given below: 
![data guardrails](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/7.data%20guardrails.jpg)

![model comparison](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/8.model%20comparison.jpg)

![model performance](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/9.model%20performance.jpg)

![dataset explorer](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/10.dataset%20explorer.jpg)

![feature importance](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/11.feature%20importance.jpg)

3. Deploy the best model

I clicked on the best model in AutoML section > Deploy > As Webservice

Model got successfully deployed:
![model deployment](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/12.model%20deployment.jpg)

4. Enable logging

Modified logs.py to enable app insights:
![logs.py](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/13.logs.py.jpg)

App insights are enbaled:
![app insights enabled](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/14.app%20insights%20enabled.jpg)

5. Swagger Documentation

Running swagger.sh to run swagger locally
![running swagger locally](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/15.running%20swagger%20locally.jpg)

This is the default swagger web ui:
![default swagger web ui](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/16.default%20swagger%20web%20ui.jpg)

serve.py is executed and it will start a Python server on port 8000. This script needs to be right next to the downloaded swagger.json file
![configured swagger web ui](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/17.configured%20swagger%20web%20ui.jpg)

6. Consume model endpoints

To use the provided endpoint.py script, replace the scoring_uri and key with the REST endpoint and primary key, respectively. The script issues a POST request to the deployed model and gets a JSON response that is printed to the terminal:
![endpoint.py](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/18.endpoint.py.jpg)

Data file getting generated after this:

![data file getting created](https://github.com/adityasant1998/azuremlnanodegree-assgn2/blob/4c19061258a714cffb27243313df51b46b6d77b6/screenshots/19.data%20file%20getting%20created.jpg)

## Screen Recording
link to a screen recording of the project in action
https://drive.google.com/file/d/1BXpX_iWLbhoYu1BVXAFiJxmCF8XOqjcF/view?usp=sharing

