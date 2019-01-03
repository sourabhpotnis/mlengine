# mlengine

## What is ML Engine?

ML Engine is a Python package providing end to end Machine learning platform. It is designed to cover the end-to-end ML workflow: Onboard new application, train, evaluate, and deploy models, make predictions, and maintain the metadata.  It provides a set of Flask APIs to be used by other applications as a service. It basically acts as a Orchestrator for the ML process flow to ease the process of moving ML model in a notebook to Production deployment.


## Main Features:

  	ML as a Platform

  	ML as a Service/API

  	ML Orchestration


## Where to get it
The source code is currently hosted on GitHub at: https://github.com/sourabhpotnis/mlengine/

    ### From PyPI
    pip install mlengine

## ML Engine Data Science process flow:

### B – S – E – M – M – A – C – D – P (based on SEMMA + CRISP-DM)

    Business and Data understanding
    
    Sampling / Creating Analytical Data Set
    
    Explore data
    
    Modify/Cleanse/Preprocess data
    
    ML Model creation
    
    Assess/Evaluate model results
    
    Compare models
    
    Deploy model
    
    Predict the unseen data

## ML Engine Core components:
API
Metadata manager
UI  
Infra
Database
ML Model

URL:	https://<server>:5001/
      https://localhost:5001/
  
  
## API Flow:

### Onboarding -> Upload -> Explore -> Training -> Predict

Model - 	GetModelsList
		      TrainModel
		      PredictModel
		      GetModelDetails

Data - 		Upload
		      Explore
		      Download

Application - AddApplication  (Level1)
              Add Key/Region/Product (Level2)
		          GetApplicationsLIst
              GetKeys/Regions/ProductsList

Algorithm -	GetAlgorithmsList


Supported algorithms:

  1. DecisionTreeClassifier    (Classification)
  2. RandomForestClassifier    (Classification)
  3. KNeighborsClassifier      (Classification)
  4. LinearRegression          (Regression)
  5. RandomForestRegressor     (Regression)
  6. KNeighborsRegressor       (Regression)
