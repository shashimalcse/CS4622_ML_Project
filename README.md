# CS4622_ML_Project_170568L


* Pandas Profiling for EDA
* SHAP and Catboost for feature selecting and feature importance
* Catboost, XGboost, RandomForest,DNN as models (Catboost performed well)
* Optuna for hyperparamter tuning

  All the data cleaning, feature engineering, feature selecting, model training, and hyperparameter tuning processes are clearly markdown in the notebook. To explore all of the columns in the data, I used pandas profiling. The data contained several columns with a high percentage of missing values. Due to the significant volume of missing values, I elected to immediately remove those columns. If the columns were too similar, I chose to drop one of the similar columns. Certain columns were identical in every way. 
I check the Tanzania longitude and latitude boundaries and figure out dataset longitude and latitude mean are close to it but some longitude and latitude values are zero. I fill those value using mean longitude and latitude. data_recorded column in this dataset just a string, i converted that into datetime and generate new 3 columns(day,month,year) using it. I replace None values in some boolean value columns using mode and other categorical columns using "Unknown". I used sklearn LabelEncoder for categorical data encoding and sklearn StandardScaler for numarical data normalization. For feature selection and feature importence i used shap library and catboost RecursiveByShapValues feature selection algorithm. I used CatBoostClassifier as my model and optuna for hyperparameter tuning. 
