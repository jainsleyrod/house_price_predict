## Singapore House Price Prediction: Project Overview
* The project estimates property prices in Singapore to help people make informed decisions when buying new houses
* Used URA API to access house data
*  Implemented modular coding throughout by creating different classes to ensure the reusability of my code
* Developed Flask application and deployed it on Render
* Link to Website: https://house-price-prediction-0uvd.onrender.com


## Resources Used
**Python Version**: 3.10
**Packages**: numpy, pandas, seaborn, requests, scikit-learn, catboost, xgboost, dill, flask
**Download Requirements**: pip install -r requirements.txt


## Data Collection
API: https://www.ura.gov.sg/maps/api/
* From the website, you can get sign up for a API key and generate API token.
Stored my data into a sqlite database to ensure efficient management and retrieval of data

Features of Data:
* propertyType
* marketSegment
* district (postal code)
* typeofSale
* area
* typeofArea
* floorRange
* contractDate
* price


## Data Ingestion
After storing my data, I did some data cleaning which included:
* converting features to correct datatype
* removing any outliers
* creating new columns like Year and Region from existing columns
* Splitting data into train test split

## Data Transformation
* Used ColumnTransformer pipeline to transform numerical and categorical columns accordingly

## Model Trainer
* Tested my data using different models like Linear Regression, Decision Tree and XGBoost
* Hyperparameter tuning to further improve results
* Evaluated my models using r2 score

**Best Model** : CatBoost

**R2 Score** : 0.8784298951068704


