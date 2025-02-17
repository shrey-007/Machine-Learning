1. It is used for both classification as well as regression, but majorly used for classification.
2. Kuch attribute ke basis pr decision lene se answer aata hai jis dataset mai unme use krte hai.
3. Ab konsa attribute uper aaega and konsa neeche vahi algorithm khud decide krta hai through mathematics.
4. The data has a hierarchical structure: Decision trees are based on a branching structure, similar to a tree. This makes them well-suited for data where relationships can be represented as a series of choices or conditions. For example, in a medical diagnosis, symptoms might be used to create a decision tree where each branch represents a possible diagnosis based on the presence or absence of certain symptoms.  



If the data is like this, then we can easily  use Logistic Regression
![img](images/Screenshot%202024-08-30%20015503.png)
But if the data is like this , then it will not work
![img](images/Screenshot%202024-08-30%20015519.png)
Suppose we want to find whether a employes's salary is greater than 10 k or not, it depends on various featues which company he works in, what's his position, what is his degree etc.
![img](images/Screenshot%202024-08-30%20015705.png)
Toh ese hierarchical decisions mai apan isko use krte hai  
Now question arises ki heirarachy mai uper kis decission ko rakhe ? We find it through entropy(randomness in data) 
Like in below image agar company ko uper rakha toh randomness kam hai(similar type output jyaada hai, like sab 10 vaale 
hi hai moslty) , but agar degree uper rakha toh randomness jyaada hai means ki kuch 10k se jyaada vaale hai kuch kam toh
iske basis par decide ni krege toh ise neeche rakhege heirarchy mai
![img](images/Screenshot%202024-08-30%20015828.png)

### Overview of Decision Tree Algorithm
A Decision Tree is a flowchart-like structure where:  

1. Root Node: The topmost node representing the entire dataset, which is split based on certain conditions.
2. Internal Nodes: These represent decisions based on a feature's value. Each internal node represents a test on a feature.
3. Branches: The outcome of a test and represent the flow from one node to another.
4. Leaf Nodes: These are the terminal nodes that represent the outcome or final decision (class label for classification or a value for regression).

### How Decision Trees Work
1. Splitting: The dataset is split into subsets based on an attribute value test. The algorithm chooses the feature that
results in the most significant information gain (for classification) or the least mean squared error (for regression).

2. Recursion: The splitting process is applied recursively to each derived subset.

Stopping Condition: The recursion stops when one of the following conditions is met:  
- All samples belong to the same class (in classification tasks).
- No further information gain can be achieved.
- A predefined depth of the tree is reached, or another stopping criterion is met (e.g., a minimum number of samples per leaf).




