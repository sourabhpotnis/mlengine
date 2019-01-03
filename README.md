# mlengine

## What is ML Engine?

ML Engine is a Python package providing end to end Machine learning platform. It is designed to cover the end-to-end ML workflow: Onboard new application, train, evaluate, and deploy models, make predictions, and maintain the metadata.  It provides a set of Flask APIs to be used by other applications as a service. It basically acts as a Orchestrator for the ML process flow to ease the process of moving ML model from a notebook to Production deployment.


## Main Features:

  	ML as a Platform<br/>
  	ML as a Service/API<br/>
  	ML Orchestration<br/>


## Where to get it
The source code is currently hosted on GitHub at: https://github.com/sourabhpotnis/mlengine/

    ### From PyPI
    pip install mlengine
    
## Starting the ML Engine
```
	### Get the location where the mlengine package is installed
	pip show mlengine | grep Location 
	### Go to the location where  mlengine package is installed
   	cd </Location/mlengine>
	### Start the ML Engine application
   	bash start_app.sh
   	### Check status of the ML Engine
	bash status_app.sh 
	### To stop the ML Engine
	bash stop_app.sh 
```
This will start the Swagger application at:
	http://server_name:5005/ or http://localhost:5005/
  

## ML Engine Core components:
**API** - Flask based APIs<br/>
**Metadata manager** - Directory structure maintained for Data Goveranance. Adviced to create own metadata store in a database
**UI** - Swagger UI to access the APIs. Advised to create own UI to access the APIs <br/>   
**Infra** - To be deployed on a UNIX box<br/>
**Database** - To store the training and prediction files in a database to be accessed by UI<br/>
**ML Model** - Machine Learning model created using Sickit-Learn<br/>


## API Flow:

**Onboarding -> Upload -> Explore -> Training -> Predict**

**Model** - 		GetModelsList
			TrainModel
			PredictModel
			GetModelDetails

**Data** - 		Upload
			Explore
			Download

**Application** - 	AddApplication  (Level1)
              		Add Key/Region/Product (Level2)
		        GetApplicationsLIst
              		GetKeys/Regions/ProductsList

**Algorithm** -		GetAlgorithmsList


## Supported algorithms:

  1. DecisionTreeClassifier    (Classification)
  2. RandomForestClassifier    (Classification)
  3. KNeighborsClassifier      (Classification)
  4. LinearRegression          (Regression)
  5. RandomForestRegressor     (Regression)
  6. KNeighborsRegressor       (Regression)