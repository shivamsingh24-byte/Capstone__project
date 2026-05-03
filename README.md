# Capstone Project - Machine Learning Model Deployment

## Project Overview

This project is an end-to-end Machine Learning system that includes data preprocessing, model training, model evaluation, and deployment using Flask. The main objective is to build a predictive system that can take user input and return real-time predictions using a trained machine learning model.

The project demonstrates the complete workflow of a data science project from data handling to production-level deployment.



## Project Structure

```
project-root/
│
├── deployment/
│   ├── app.py
│   ├── model.pkl
│   ├── config.py
│   ├── requirements.txt
│
├── notebook/
│   ├── training.ipynb
│
├── data/
│   ├── dataset.csv
│
├── presentation/
│   ├── PPT.pptx
│   ├── project_report.pdf
│
└── README.md
```


## Objectives

* To build a machine learning model using a dataset.
* To preprocess and clean the data for better accuracy.
* To train and evaluate the model using appropriate algorithms.
* To save the trained model using pickle.
* To deploy the model using Flask for real-time predictions.


## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Scikit-learn
* Flask
* Pickle


## Dataset Description

* The dataset contains input features and target labels.
* Data preprocessing is performed to handle missing values and categorical encoding.
* The dataset is split into training and testing sets for model evaluation.


## Model Building Process

* Data is loaded and preprocessed.
* Features are selected and cleaned.
* Machine learning algorithms such as Logistic Regression or Random Forest are used.
* The model is trained on the training dataset.
* Performance is evaluated using accuracy and other metrics.


## Model Saving

After training, the model is saved using pickle for deployment.

```python
import pickle
pickle.dump(model, open("model.pkl", "wb"))
```


## Deployment Process

The trained model is deployed using Flask API.

### Steps:

1. Load the saved model in `app.py`.
2. Create Flask routes for API requests.
3. Accept user input through POST request.
4. Process input and pass it to the model.
5. Return prediction as JSON response.


## Running the Project

### Install Dependencies

```
pip install -r requirements.txt
```

### Run Flask Application

```
python app.py
```

### Access Application

Open browser and go to:

```
http://127.0.0.1:5000/
```


## API Details

### Endpoint

```
/predict
```

### Method

POST

### Input Format

```json
{
  "input": [value1, value2, value3]
}
```

### Output Format

```json
{
  "prediction": "result"
}
```


## System Workflow

1. User sends input through API.
2. Flask receives the request.
3. Model is loaded from model.pkl.
4. Prediction is generated.
5. Response is returned to the user.


## Results

* The model successfully generates real-time predictions.
* The system is tested using Postman and browser.
* The deployment is functional and stable.


## Advantages

* Real-time prediction system
* Easy integration with web applications
* Scalable architecture
* End-to-end machine learning pipeline


## Limitations

* Performance depends on dataset quality
* Model requires retraining for new data
* Basic deployment without cloud integration


## Future Scope

* Deployment on cloud platforms like AWS or Render
* Integration with frontend interface
* Improvement of model accuracy
* Database integration for storing predictions
* Mobile application integration


## Conclusion

This project successfully demonstrates an end-to-end machine learning pipeline including data preprocessing, model training, and deployment using Flask. It provides real-time predictions and can be extended for production-level applications in various domains.
