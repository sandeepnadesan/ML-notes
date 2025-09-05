## It is a branch of AI where it is used to build models and it is used to train the computer with the help  of data provided.

![[Pasted image 20250904092307.png]]

![[Pasted image 20250904092319.png]]
![[Pasted image 20250904092329.png]]


## They are classified into 3 types
 ### Supervised Learning -> with the help of labelled dataset
 ## Unsupervised Learning -> without labelled dataset
 ## Reinforcement Learning -> Learns through trial and error to maximize rewards.

## Supervised Learning
The model learns by comparing its predictions with the actual answers provided in the training data.

- ****Training Data:**** The model is provided with a training dataset that includes input data (features) and corresponding output data (labels or target variables).
- ****Learning Process:**** The algorithm processes the training data, learning the relationships between the input features and the output labels. This is achieved by adjusting the model's parameters to minimize the difference between its predictions and the actual labels.
To check the validation we can use 
## Cross-Validation:
It is used to check the how the model performs in unseen data.
It splits the data into train and test part and and keep on training the model
It is used to prevent overfittting

####  Holdout Validation

In [Holdout Validation](https://www.geeksforgeeks.org/software-engineering/introduction-of-holdout-method/) we perform training on the 50% of the given dataset and rest 50% is used for the testing purpose. It's a simple and quick way to evaluate a model. The major drawback of this method is that we perform training on the 50% of the dataset, it may possible that the remaining 50% of the data contains some important information which we are leaving while training our model that can lead to higher bias.

#### LOOCV (Leave One Out Cross Validation)

In this method we perform training on the whole dataset but leaves only one data-point of the available dataset and then iterates for each data-point. In [LOOCV](https://www.geeksforgeeks.org/r-language/loocvleave-one-out-cross-validation-in-r-programming/) the model is trained on n−1n−1 samples and tested on the one omitted sample repeating this process for each data point in the dataset. It has some advantages as well as disadvantages also.

- An advantage of using this method is that we make use of all data points and hence it is low bias.
- The major drawback of this method is that it leads to higher variation in the testing model as we are testing against one data point. If the data point is an outlier it can lead to higher variation.
- Another drawback is it takes a lot of execution time as it iterates over the number of data points we have.

### Overfitting 
### Performs good in training and not good in test data
1. It learns patterns effectively from the training data.
2. It generalizes well to new, unseen data.
3. It avoids memorizing the training data (overfitting) or failing to capture relevant patterns (underfitting).
4. Overfitting happens when a model learns too much from the training data, including details that don’t matter (like noise or outliers).
****Reasons for Overfitting:****

1. High variance and low bias.
2. The model is too complex.
3. The size of the training data.

## Underfitting
### Performs bad in both train and test data
****Reasons for**** ****Underfitting:****

1. The model is too simple, So it may be not capable to represent the complexities in the data.
2. The input features which is used to train the model is not the adequate representations of underlying factors influencing the target variable.
3. The size of the training dataset used is not enough.
4. Excessive regularization are used to prevent the overfitting, which constraint the model to capture the data well.
5. Features are not scaled.


## Bias and Variance in Machine Learning
****Bias****: is the error that happens when a machine learning model is too simple and doesn't learn enough details from the data. It's like assuming all birds can only be small and fly, so the model fails to recognize big birds like ostriches or penguins that can't fly and get biased with predictions.

- High bias typically leads to ****underfitting****, where the model performs poorly on both training and testing data because it fails to learn enough from the data.
****Variance****: Error that happens when a machine learning model learns too much from the data, including random noise.

- A high-variance model learns not only the patterns but also the noise in the training data, which leads to poor generalization on unseen data.
-  High variance typically leads to ****overfitting****, where the model performs well on training data but poorly on testing data.
![[Pasted image 20250904094653.png]]

### ****Techniques to Reduce Underfitting****

1. Increase model complexity.
2. Increase the number of features, performing [feature engineering](https://www.geeksforgeeks.org/machine-learning/what-is-feature-engineering/).
3. Remove noise from the data.
4. Increase the number of [epochs](https://www.geeksforgeeks.org/machine-learning/epoch-in-machine-learning/) or increase the duration of training to get better results.

****Techniques to Reduce Overfitting****

1. Improving the quality of training data reduces overfitting by focusing on meaningful patterns, mitigate the risk of fitting the noise or irrelevant features.
2. Increase the training data can improve the model's ability to generalize to unseen data and reduce the likelihood of overfitting.
3. Reduce model complexity.
4. [Early stopping](https://www.geeksforgeeks.org/machine-learning/regularization-by-early-stopping/) during the training phase (have an eye over the loss over the training period as soon as loss begins to increase stop training).
5. [Ridge Regularization](https://www.geeksforgeeks.org/machine-learning/lasso-vs-ridge-vs-elastic-net-ml/) and [Lasso Regularization](https://www.geeksforgeeks.org/machine-learning/implementation-of-lasso-regression-from-scratch-using-python/).
6. Use [dropout](https://www.geeksforgeeks.org/machine-learning/dropout-in-neural-networks/) for [neural networks](https://www.geeksforgeeks.org/machine-learning/neural-networks-a-beginners-guide/) to tackle overfitting.