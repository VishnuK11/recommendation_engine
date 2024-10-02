#  Installation
- Use the requirements.txt to install the required dependencies

# Prerequisite
- Ensure the training data folder, `ml-100k` is present in base path

# Usage
- Use following code snippet to retrieve prediction
```
ms = ModelServing() 
pred = ms.model_predict((<user_id>, <item_id>, 0.0))
```
- Endpoint: POST `http://127.0.0.1:5001/predict_one` 
- json_data = {`user_id`: <user_id>, `item_id`: <item_id>}

# About Model
- Used SVD based collaborative filtering trained on features of u.data: `user_id`, `item_id`, `rating`
- Used a package `Surprise` 
- Hyperparameter tuned using  GridSearchCV
- Contains 8 Tests
