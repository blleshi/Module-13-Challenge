# Neural Network Binary Classification Challenge

## Instructions
The instructions for this challenge are divided into the following sections:

### Prepare the Data for Use on a Neural Network Model
Using your knowledge of Pandas and `StandardScaler` from `scikit-learn`, preprocess the dataset for compiling and evaluating the neural network model. Complete the following steps:

1. Read the `applicants_data.csv` file into a Pandas DataFrame. Review the DataFrame, checking for categorical variables that need encoding and identifying columns that will define your features and target variables.
2. Drop the “EIN” (Employer Identification Number) and “NAME” columns from the DataFrame, as they’re irrelevant for the binary classification model.
3. Encode the categorical variables using `OneHotEncoder` and place the encoded variables in a new DataFrame.
4. Add the numerical variables from the original DataFrame to the DataFrame containing the encoded variables.
   - **Note**: Use the Pandas `concat` function to complete this step.
5. Using the preprocessed data, create the features (X) and target (y) datasets. The “IS_SUCCESSFUL” column in the preprocessed DataFrame should define the target dataset. The remaining columns should define the features dataset.
6. Split the features and target datasets into training and testing datasets.
7. Use `StandardScaler` from `scikit-learn` to scale the features data.

### Compile and Evaluate a Binary Classification Model Using a Neural Network
Design a binary classification deep neural network model using TensorFlow. This model should use the features of the dataset to predict whether a startup funded by Alphabet Soup will become successful. Consider the number of inputs before determining the number of layers and neurons on each layer. Then compile and fit your model. Finally, evaluate your binary classification model to calculate the model’s loss and accuracy. Complete the following steps:

1. Use TensorFlow’s Keras to create a deep neural network by assigning the number of input features, layers, and neurons on each layer.
2. Compile and fit the model using the `binary_crossentropy` loss function, the `adam` optimizer, and the `accuracy` evaluation metric.
3. Evaluate the model using the test data to determine the model’s loss and accuracy.
4. Save and export your model to an HDF5 file, naming the file `AlphabetSoup.h5`.

### Optimize the Neural Network Model
Optimize your model to improve its accuracy using TensorFlow and Keras. Even if you don’t achieve better accuracy, demonstrate at least two attempts to optimize the model. Include these attempts in your existing notebook, or make copies of the starter notebook, renaming them, and code each model optimization in a new notebook. Complete the following steps:

1. Define at least three new deep neural network models (the original plus two optimization attempts). For each, try to improve your first model’s predictive accuracy.
2. Display the accuracy scores each model achieved, and then compare the results.
3. Save each model as an HDF5 file.
