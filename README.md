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


3. Deploy the best model
4. Enable logging
5. Swagger Documentation
6. Consume model endpoints
7. Create and publish a pipeline

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
