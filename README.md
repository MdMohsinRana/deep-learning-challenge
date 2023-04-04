# deep-learning-challenge

Deep Learning

Alphabet Soup Charity Model
Overview of the Analysis
In this analysis, we used a real-world dataset containing data from over 35,000 organizations funded by Alphabet Soup in the past. Our goal was to create a deep learning neural network model to predict the success or failure of future funding initiatives.

Results
Data Preprocessing
The "IS_SUCCESSFUL" column serves as the target variable for this model.
During optimization attempts, different feature sets were explored to understand their impact on loss and accuracy.
For all optimization attempts, the "EIN" and "NAME" variables were removed.
Compiling, Training, and Evaluating the Model
The main model consists of two hidden layers with 80 and 30 neurons, respectively. The hidden layers use the "relu" activation function, while the output layer employs the "sigmoid" activation function. The model was trained over 100 epochs.

The main model did not achieve the target performance of 75%. Its accuracy was approximately 72.76%, with a loss of 55.85%.

To increase model performance, three different optimization attempts were made:

Attempt #1

The number of epochs was increased from 100 to 150.
An additional hidden layer with 60 neurons was introduced.
The binning structure of the "CLASSIFICATION" column was modified.
More neurons were added to the hidden layers.
Results: 72.44% accuracy (worse) / 59.79% loss (worse)

Attempt #2

The 'STATUS' and 'SPECIAL_CONSIDERATION' variables were dropped.
The binning structures of the 'APPLICATION_TYPE' and 'CLASSIFICATION' variables were altered.
A new hidden layer with 60 neurons was added.
Results: 72.60% accuracy (worse) / 57.90% loss (worse)

Attempt #3

Two more dense layers were added.
Results: 73.01% accuracy (better) / 55.82% loss (better)

Summary
None of the optimization attempts achieved a significant increase in accuracy; in fact, some led to an increase in loss. Given the abundance of categorical data in our dataset, it may be worthwhile to explore decision tree or random forest methods for potentially better results. Overall, Attempt #3 had a slight positive influence on the model's performance.
