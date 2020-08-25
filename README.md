# Pima-Indians-Diabetes-prediction

The dataset for this programe was taken from kaggel, you can dwonload the dataset from [here](https://www.kaggle.com/uciml/pima-indians-diabetes-database)


# About the dataset 

The dataset is a '.csv' file containing the features and outcome/target variable which is 0/1 depending on whether the person has diabetes or not.
Our task is to make a model to predict for some test data whether the person has diabetes or not.
If you have a look at the dataset, the data is very less with only around 768 examples and 8 features for the feature variable. So we will train our model only on 760 examples and test on the remaining 8 data samples.

# About the made model

The model code that you see in the jupyter notebook was written using the 'PyTorch' Framework. You can refer to the docs of PyTorch (https://pytorch.org/docs/stable/index.html).
In the model I have only used 3 layers(1-input, 1-hidden and 1-output layer). The model is trained on 760 training examples and is validated on the remaining 8 examples.
If you have a look the model is trained for 1000 'EPOCHS;. Now when you predict the output for a given input, the output predicted by the model is the probability score for the input(in the range 0 to 1). Now I considered if the probability is greater than 0.5(50%) then the 'target' will be '1' else it will be '0'.
Now this threshold value that was 50% for me you can change this to any value(Say 0.9 for 90% confidence depending). 
I first caluclated the training accuracy which was some where around '92%', Then i validated the model over the test data and the accuray was around '87.5%'.
I saved this model with the name 'Model1.pth' which is the pytorch format of saving a model for future use. The last code of the notebook shows how you can load the saved model.

I have also uploades the 'Model1.pth' in this repo as well.

