The **Naive Bayes Classifier** is a simple yet powerful algorithm based on applying Bayes' theorem with strong (naive) independence assumptions between the features. It is particularly popular for tasks like text classification (e.g., spam detection, sentiment analysis) due to its effectiveness, simplicity, and speed.

It is supervised learning algorithm

### How Naive Bayes Classifier Works

1. **Bayes' Theorem**: The Naive Bayes classifier is based on Bayes' theorem, which describes the probability of a hypothesis (in this case, a class label) given some observed evidence (the feature values). The formula for Bayes' theorem is:

\[
P(C|X) = \frac{P(X|C) \cdot P(C)}{P(X)}
\]


where:
- \(P(C|X)\) is the posterior probability of class \(C\) given the features \(X\).
- \(P(X|C)\) is the likelihood of observing features \(X\) given class \(C\).
- \(P(C)\) is the prior probability of class \(C\).
- \(P(X)\) is the prior probability of observing the features \(X\).

2. **Naive Assumption of Independence**: The "naive" part of the algorithm assumes that all features are independent of each other given the class label. This simplifies the calculation of the likelihood \(P(X|C)\) as:

\[
P(X|C) = P(x_1|C) \cdot P(x_2|C) \cdot \ldots \cdot P(x_n|C)
\]

where \(X = (x_1, x_2, \ldots, x_n)\) are the individual features.

3. **Prediction**: To predict the class of a new observation, the algorithm calculates the posterior probability for each class and selects the class with the highest probability:

\[
\text{Predicted Class} = \arg \max_{C} P(C|X)
\]

### Types of Naive Bayes Classifiers

1. **Gaussian Naive Bayes**: Assumes that the features are normally distributed. It is often used for continuous data.

2. **Multinomial Naive Bayes**: Suitable for discrete data, such as word counts or frequencies in text classification.

3. **Bernoulli Naive Bayes**: Designed for binary/boolean features. It's also used in text classification where the feature is a binary term indicating the presence or absence of a word.







### Key Advantages of Naive Bayes Classifier

- **Simple and Fast**: Easy to implement and fast to train, even on large datasets.
- **Performs Well with Small Data**: Can perform surprisingly well with small amounts of data, especially in cases of text classification.
- **Handles High-Dimensional Data**: Particularly effective for high-dimensional data, like text, due to its assumption of feature independence.

### Limitations

- **Assumes Feature Independence**: The assumption that all features are independent given the class label may not always hold true, which can affect its performance.
- **Not Suitable for Correlated Features**: If features are highly correlated, Naive Bayes may not perform well.
- **Zero Probability Issue**: If a feature was not present in the training data for a particular class, the probability can become zero. This can be handled using techniques like Laplace smoothing.

Would you like more details on a specific type of Naive Bayes, or an example in another language?


## Take an example of dataset of titanic survivors
Let's use the **Titanic Survivor** dataset with two input features: **sex** and **age**, and the output is whether the passenger **survived** or **not**.

### 1. **Problem Setup**

- **Features** (`X`):
    - `sex`: Male or Female
    - `age`: Age of the passenger
- **Target** (`C`): `survived` (Yes or No)

### 2. **Bayes' Theorem**

We want to compute the probability of survival (`C`) given `sex` and `age` (`X`):

\[
P(\text{survived} \,|\, \text{sex, age}) = \frac{P(\text{sex, age} \,|\, \text{survived}) \cdot P(\text{survived})}{P(\text{sex, age})}
\]

- **Posterior**: \( P(\text{survived} \,|\, \text{sex, age}) \)
- **Likelihood**: \( P(\text{sex, age} \,|\, \text{survived}) \)
- **Prior**: \( P(\text{survived}) \)
- **Evidence**: \( P(\text{sex, age}) \) (constant for all classes, so it can be ignored in practice)

### 3. **Naive Assumption of Independence**

Assume `sex` and `age` are independent given survival:

\[
P(\text{sex, age} \,|\, \text{survived}) = P(\text{sex} \,|\, \text{survived}) \cdot P(\text{age} \,|\, \text{survived})
\]

### 4. **Calculating the Posterior Probability**

To predict if a passenger survives, we calculate:

\[
P(\text{survived} = \text{Yes} \,|\, \text{sex, age}) \propto P(\text{sex} \,|\, \text{survived} = \text{Yes}) \cdot P(\text{age} \,|\, \text{survived} = \text{Yes}) \cdot P(\text{survived} = \text{Yes})
\]

\[
P(\text{survived} = \text{No} \,|\, \text{sex, age}) \propto P(\text{sex} \,|\, \text{survived} = \text{No}) \cdot P(\text{age} \,|\, \text{survived} = \text{No}) \cdot P(\text{survived} = \text{No})
\]

### 5. **Step-by-Step Calculation Example**

- **Prior Probabilities**: Calculate from the dataset:
    - \( P(\text{survived} = \text{Yes}) = \frac{\text{Number of survivors}}{\text{Total passengers}} \)
    - \( P(\text{survived} = \text{No}) = \frac{\text{Number of non-survivors}}{\text{Total passengers}} \)

- **Likelihoods**:
    - \( P(\text{sex} = \text{Female} \,|\, \text{survived} = \text{Yes}) = \frac{\text{Number of female survivors}}{\text{Total survivors}} \)
    - \( P(\text{age} = 30 \,|\, \text{survived} = \text{Yes}) = \frac{\text{Number of survivors aged 30}}{\text{Total survivors}} \)  
      (Use probability density for continuous variables like age if needed)

- **Compute Posterior for Both Classes**:  
  Compare \( P(\text{survived} = \text{Yes} \,|\, \text{sex, age}) \) and \( P(\text{survived} = \text{No} \,|\, \text{sex, age}) \).

- **Prediction**: Choose the class with the higher posterior probability.

This method will give you the most probable class (survived or not) based on the given inputs of `sex` and `age`.