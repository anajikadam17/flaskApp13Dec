## Used Car Selling Price Suggester

This web app uses a Random Forrest Regressor model to suggest a suitable price for used cars. The model is trained on the CarDekho dataset available [here](https://www.kaggle.com/nehalbirla/vehicle-dataset-from-cardekho) on Kaggle. 


### Project Structure

This project has four major parts :

1. used_car_price_suggester.ipynb - This notebook contains the code for EDA, model creation, and training.
2. app.py - This contains the Flask API that receives car details through API calls, computes the precited price based on our model, and returns it.
3. random_forest_regression_model.pkl - A serialized(```pickle```d) version of the Random Forrest Regressor model so we can simply load it and make suggestions.
4. templates - This folder contains the HTML template to allow the user to enter car details and get a price suggestion.

### Running the project
1. Ensure that you have installed all the dependencies from ```requirements.txt```. Run all the cells of the notebook to create a new model or simply use the serialized version of our model random_forest_regression_model.pkl

2. Go to the project directory and app.py using the below command to start Flask API
```
python app.py
```
By default, the Flask app will run on port 5000.

3. Navigate to URL http://localhost:5000 or http://127.0.0.1:5000/