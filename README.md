# deep-learning-challenge
Report on the Neural Network Model:
Overview
In this report, we analyze the performance of a neural network model designed to predict the success of the applicats for funding with the best chance of success.  

Data Preprocessing
The data was processed with StandardScaler() by reading the csv file.  To clean up the unnecessary data, we have dropped EIN and NAME columns and combined some of the values that has a certain cuttoff amount.
pd.get_dummies() was used to convert the categorical variables to the numeric to split the features(X) and target (y). The target y was set for the column that give the result of whether the orignization is successufll or not.

Model Architecture
The original model using one hidden layer plus input and output layer with 5 epochs while the optimized model used two hidden layer with input and output and 100 epochs.  The comparison of the model shows how the result would differ.

Training and Evaluation
The model was trained and evaluated the model's performance on the test data by calculating accuracy and loss.

Result Analysis:
The original model with 5 epochs and only 1 hidden middle layer only has model accuracy of 0.5336 with loss 0.69.  Since it only has 5 total epochs, the process does not take long but the accuracy is not reliable.
The optimized model with 100 epochs with two hidden layers came out with accuracy of 0.7273 with loss 0.57.  This took a lot longer but the accuracy has increased drastically. 

References: 
XpertLearning for warnings fixes:
X_train_scaled_reshaped = X_train_scaled[:, :2]
nn.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'], run_eagerly=True)
Lectures
