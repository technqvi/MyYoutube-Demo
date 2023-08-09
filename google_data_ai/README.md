## Tutorial#1 - [t1-import-incident-postgres_to_bigquery.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t1-import-incident-postgres_to_bigquery.ipynb "t1-import-incident-postgres_to_bigquery.ipynb")
- Export data stored on Postgres Database and Ingest it into BigQuery using Bigquery Python.Client Library
- Create dataset and table fundamentally on Google Console
- [YouTube Tutorial : 1 Export Data To BigQuery Using Python](https://www.youtube.com/watch?v=kgEe4Fb1s1U&t=2011s)

## Tutorial#2 - [t2-explore_to_create_train_data_ml.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t2-explore_to_create_train_data_ml.ipynb "t2-explore_to_create_train_data_ml.ipynb")
- Retrieve data from BigQuery to prepare data for building Machine Learning.
- Explore & Analyse data with basic statictical method.
- Transform raws data to be more informative and select columns as engineered featured for ML .
- Split Data into Train , Validation and Test Data DataSet and  Ingest them into BigQuery
- [YouTube Tutorial : 2 Exlore Data To Build Traing DataSet For ML](https://www.youtube.com/watch?v=Uzh5Wc4yZSQ)

## Tutorial#3 - [t3-build_train_model.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t3-build_train_model.ipynb) | [t3-transform-data.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t3-transform-data.ipynb)
- Get train ,validation and test data from BigQuery as dataframe.
- Covert dataframe to tensorflow as data on tf.data input pipeline
- Normalize numberical value and perform onehot-encoding on Keras Preprocessing Layer.
- Build model with Keras API.
- Train model and evaluate model on validation data and test data.
- Save Model to local path and export it to GCS.
- Reload model to predict data.
- [YouTube Tutorial : 3 Build Tensorflow with Keras API Model To Predict Severity Level of Incident](https://www.youtube.com/watch?v=ycDBWiXzZqQ)


## Tutorial#4 - [t4-tuning_train_model.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t4-tuning_train_model.ipynb )
Use keras-tuner to find optimal hypter paramter to get best mode ( we improve model performamce from [t3-build_train_model.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t3-build_train_model.ipynb) ).
- [YouTube Tutorial : 4 Tuning Model With Keras Tuner](https://www.youtube.com/watch?v=uDwrhbMMPxw)


## Tutorial#5 -[t5-binary_train.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t5-build_train_binaryclass_model.ipynb) | [t5-binary_evaluation.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t5-evaluate-binary_model-prediction-data.ipynb) | [t5-evaluate-model-prediction-on-test-data.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t5-evaluate-model-prediction.ipynb)
- Exlain metrics to evaluatte model focusing on Accuracy.
- Demo how to to evaluate model by getting started with binary classification.
- Demo how to to evaluate model on muticlass classification.
- Describe how balanced data and imbalaned data lead to model's performance
- [YouTube Tutorial : 5 Evaluate Model with Accuracy Metric](https://www.youtube.com/watch?v=itfTFz4e7tg)

## Tutorial#6 - [t5-evaluate-model-prediction-on-test-data.ipynb](https://github.com/technqvi/MyYoutube-Demo/blob/main/google_data_ai/t5-evaluate-model-prediction.ipynb) : Deploy Model to VertextAI Section
 - Register model stored on GCS to Model Registry.
 - Deploy model endpoint as Online.
 - Deploy model as batch prediction.
 - [YouTube Tutorial : 6 Register and Deploy Model From Local Dev to Vertext-AI](https://www.youtube.com/watch?v=7Ee7j-lEHBY)
 
 ## Tutorial#7 - [t7-load-new-incident-ml](https://github.com/technqvi/MyYoutube-Demo/tree/main/google_data_ai/t7-load-new-incident-ml) : Cloud Function and Scheduler
 - Export data from incident  table to new_incident
 - This folder is structure to deploy cloud function created with VS Code.
 - Run this command  on Google Cloud SDK Shell to test function:   functions-framework --target=load_new_incident_ml_to_bq 
 - Run this command on Google Cloud SDK Shell to deoploy function: gcloud functions deploy load-new-incident-ml-to-bq  --gen2  --region=asia-southeast1  --runtime=python39  --memory=512 --source=.  --env-vars-file .env.yaml  --trigger-http   --entry-point  load_new_incident_ml_to_bq
 - [YouTube Tutorial : 7 Load New Incident To Get Prepared For Making a Prediction](https://www.youtube.com/watch?v=uR23WkS8XjQ)
 
  ## Tutorial#8 - [t8-predict_incident_severity](https://github.com/technqvi/MyYoutube-Demo/tree/main/google_data_ai/t7-load-new-incident-ml) : Cloud Function and Scheduler
 - Load data from new_incident.
 - Load model from google data storage.
 - Predict new incident data.
 - Store prediction result data on anothor table.
 - Test and Deploy Cloud function as prev tutorial.
 - [YouTube Tutorial : 8 8 Making Prediction On New Incident](https://www.youtube.com/watch?v=kCgyMRXmaTs&feature=youtu.be)