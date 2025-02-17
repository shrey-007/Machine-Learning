### Define Bias and Variance.
Bias

When a model makes predictions, a disparity between the model's prediction values and actual values arises, and this difference is known as bias. Bias is the incapacity of machine learning algorithms like Linear Regression to grasp the real relationship between data points.

Variance

If alternative training data were utilized, the variance would describe the degree of variation in the prediction. In layman's terms, variance describes how far a random variable deviates from its predicted value.

### You have come across some missing data in your dataset. How will you handle it?
In order to handle some missing or corrupted data, the easiest way is to just replace the corresponding rows and columns, which contain the incorrect data, with some different values. The two most useful functions in Panda for this purpose are isnull() and fillna().

isnull(): is used to find missing values in a dataset  
fillna(): is used to fill missing values with 0’s  

We can do following with the data having missing values-:
1. Remove the rows
2. Fill the missing value with mean/median
3. Fill all missing values with a constant like 0


### How is a logistic regression model evaluated?
One of the best ways to evaluate a logistic regression model is to use a confusion matrix, which is a very specific table that is used to measure the overall performance of any algorithm.

Using a confusion matrix, you can easily calculate the Accuracy Score, Precision, Recall, and F1 score. These can be extremely good indicators for your logistic regression model.

If the recall of your model is low, then it means that your model has too many False Negatives. Similarly, if the precision of your model is low, it signifies that your model has too many False Positives. In order to select a model with a balanced precision and recall score, the F1 Score must be used.

### To start Linear Regression, you would need to make some assumptions. What are those assumptions?
1. Linear relationship bw target(feature that need to be predicted) and features
2. features are independent to each other

### Difference bw AI and ML
Artificial Intelligence is a system of producing intelligent machines that can imitate human intelligence. Machine Learning is training machines to learn from present data and act on these experiences in the future.

### Differentiate between Deep Learning and Machine Learning?
Machine Learning adopts algorithms to learn from data sets and apply this to future decision making. Deep Learning is a subset of Machine Learning that uses large amounts of data and complex algorithms to create neural networks that can learn and make decisions on their own

### what is cross validation
Cross-validation is a statistical technique used in machine learning to evaluate the performance of a model. It involves partitioning the original dataset into multiple subsets (or "folds") and then training and testing the model on different subsets to ensure that it generalizes well to new, unseen data.

### What are the types of Machine learning?
There are mainly three types of Machine Learning, viz:

Reinforcement learning: It is about taking the best possible action to maximize reward in a particular scenario. It is used by various software and machines to find the best path it should take in a given situation.

Supervised learning: Using labeled datasets to train algorithms to classify data easily for predicting accurate outcomes.

Unsupervised learning: It uses ML to analyze and cluster unlabeled datasets.

### What is the difference between correlation and causality?
Correlation is the relation of one action (A) to another action (B) when A does not necessarily lead to B, but Causality is the situation where one action (A) causes a result (B). Naam se pata pad rha hai A , B ka cause hai

### What is the difference between Correlation and Covariance?
Correlation quantifies the relationship between two random variables with three values: 0,1 and -1.
Covariance is the measure of how two different variables are related and how changes in one impact the other

### What are the requirements of reinforcement learning environments?
State, reward data, agent, and environment. It is entirely different from other machine learning paradigms. Here we have an agent and an environment. The environment refers to a task or simulation; the agent is an algorithm that interacts with the environment and tries to solve it.

### List the differences between KNN and k-means clustering.
| KNN                                    | k-means clustering      |
|----------------------------------------|-------------------------|
| Used for classification and regression | Used for classification | 
| Supervised                             | Unsupervised            | 

### What is semi-supervised learning?
A semi-supervised learning happens when a small amount of labeled data is introduced to an algorithm. The algorithm then studies that data and uses it on unlabeled data. Semi-supervised learning combines the efficiency of unsupervised learning and the performance of supervised learning.

### What is PCA
PCA means Principal Component Analysis, and is mainly used for dimension reduction. It is a statistical technique used to reduce the dimensionality of large datasets while retaining as much information as possible. In other words, it identifies patterns and correlations among variables and summarizes them into a smaller set of uncorrelated variables called principal components.

### What are support vectors in SVM (Support Vector Machine)?
Support vectors are the data points in a dataset that are closest to the hyperplane (the line that separates the classes in the dataset) and are used to build the classifier.

### What is the difference between Regression and Classification?
Classification is a concept used to produce discrete results and to classify data into specific regions. On the other hand, regression is used to assess the relationship between independent variables and dependent variables.It results in continuous values

### What is a neural network?
Much like a human brain, the neural network is a network of different neurons connected in a way that helps information flow from one neuron to the other. It is a function that maps input to desired output with a given set of inputs. Structurally, it is organized into an input layer, an output layer, and one or more hidden layers.

### What is ensemble learning?
Ensemble learning is a method that merges multiple machine learning models to create various powerful models. The aim is to provide better performance by combining models rather than sticking to a single model.

### What is overfitting?
Overfitting is said to happen when a statistical model observes and learns the details in the training data to the point that it starts negatively impacting the model's performance on new datasets.

### What is dimension reduction in ML?
Dimension reduction is the reduction of variables put under consideration. It lessens the number of features in a dataset while saving as much information as possible. This can be done for various reasons, such as to improve the performance of a learning algorithm, reduce the complexity of a model, or make it easier to visualize the data.

### What is underfitting?
Underfitting is a type of error in ML models where the model fails to capture the underlying pattern of the data. It occurs when a model is too simplistic and is unable to capture the complexity of the data, leading to poor generalization performance on unseen data. In other words, the model is not complex enough to accurately capture the relationship between the input and output variables. This often leads to high bias and low variance.

### What is time series
A time series is a sequence of data points collected or recorded at specific time intervals. These data points typically represent the evolution of a variable over time, such as daily stock prices, monthly sales figures, annual GDP growth rates, or temperature measurements taken every hour.

Key Characteristics of Time Series:
1. Temporal Order:
The data points in a time series are arranged in chronological order. The order is crucial because it reflects how the data evolves over time.
2. Regular Intervals:
Time series data is usually recorded at regular time intervals, such as every minute, hourly, daily, weekly, monthly, or annually.
3. Dependence:
Time series data often exhibits temporal dependence, meaning that current observations are dependent on past observations

Applications of Time Series Analysis: Stock Market, Weather Forecasting

### Why is the Naive Bayes Method ‘Naive’?
The Naive Bayes is called naive because, as a supervised learning algorithm, it makes assumptions by applying the Bayes Theorem that all attributes are independent of each other

### What is difference between recission and recall

### How to detect outlier
Using z score, Box plot

### Why is the ROC in a curve important?
The ROC curve is important because it is a visual representation of how well a model can distinguish between two classes, and it can be used to compare different models. The area under the curve (AUC) is a measure of how well the model performs, with a higher AUC indicating a better model. Additionally, the shape of the curve can indicate whether a model is biased towards one class or another.

### Why does overfitting occur in ML?
Overfitting occurs in ML when the model is too complex or has too many parameters relative to the amount of data that is available. This causes the model to fit the noise of the data rather than the underlying patterns, resulting in poor generalization and an inability to accurately predict on previously unseen data.

### What is Regularization in ML?
Regularization is a technique used to prevent overfitting in ML models. Overfitting occurs when a model is too complex and fits the training data too closely, resulting in poor performance on new, unseen data. Regularization techniques add a penalty term to the model's objective function, which encourages the model to find simpler solutions by reducing the magnitude of the coefficients or parameters in the model. This reduces the model's ability to fit the noise in the training data, resulting in better generalization performance on new data. Some popular regularization techniques include L1 (lasso) and L2 (ridge) regularization, which differ in the way they penalize the coefficients.

### What ensemble techniques can be used to aggregate multiple models?
Two ensemble techniques that can be used include Bagging and Boosting:

Bagging ((Bootstrap Aggregating): It is a technique where multiple independent models are trained on different subsets of the training data, and their predictions are aggregated to form the final prediction. The idea behind bagging is to reduce the variance of the model by averaging over multiple models.

Boosting: This is an iterative ensemble technique where the models are trained sequentially, and each subsequent model is trained on the instances where the previous model performed poorly. The idea behind boosting is to reduce the bias of the model by focusing on the misclassified instances

### Do you think logistic regression can be used for more than two classes?
No. Logistic regression is a binary classifier; thus, it cannot be applied to more than two classes. However, it can be employed in multinomial logistic regression of solving multi-class classification problems.

### How can overfitting be avoided in ML?

Some of the methods that you can use to avoid overfitting in machine learning are:

1. Cross validation
2. Custom feature selection
3. Data augmentation
4. Using larger datasets
5. Data simplification
6. Ensembling
7. Regularization

### How would you handle a dataset suffering from high variance?
The bagging algorithm can be used to split the data into subgroups sampling replicated from random data. After this split, the random data is utilized to establish rules using a training algorithm. Thereafter, the polling technique is used to combine all the predicted outcomes of the model.


