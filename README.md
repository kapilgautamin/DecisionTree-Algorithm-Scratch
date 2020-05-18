**Problem 1**: Implement a fixed-depth decision tree algorithm, that is, the input to the ID3 algorithm
will include the training data and maximum depth of the tree to be learned.

**Data Sets**: The data sets (in the folder ./data/) are obtained from the UCI Repository and are collectively
the MONK's Problem. These problems were the basis of a first international comparison of learning algorithms. The training and test files for the three problems are named monks-X.train and monks-X.test.
There are six attributes/features (columns 2-7 in the raw files), and the class labels (column 1). There are
2 classes. Refer to the file ./data/monks.names for more details.

- For depth = 1,..., 10, learn decision trees and compute the average
training and test errors on each of the three MONK's problems. Make three plots, one for each
of the MONK's problem sets, plotting training and testing error curves together for each problem,
with tree depth on the x-axis and error on the y-axis.
- For monks-1, report the learned decision tree and the confusion
matrix on the test set for depth=1 and depth=2. 

A confusion matrix is a table that is used to
describe the performance of a classifier on a data set. For binary classification problems, it will be

|        	|          	| Classifier      	| Prediction      	|   
|--------	|----------	|-----------------	|-----------------	|
|        	|          	| Positive        	| Negative        	|   
| **Actual** 	| Positive 	| True Positive   	| False Negatives 	|
| **Values** 	| Negative 	| False Positives 	| True Negatives  	|

- For monks-1, use scikit-learns's default decision tree algorithm to learn
a decision tree. Visualize the learned decision tree using graphviz
- Report the visualized decision
tree and the confusion matrix on the test set. Do not change the default parameters.
- Repeat steps 2 and 3 with your "own" data set and report the confusion
matrices. You can use other data sets in the UCI repository. If you encounter continuous features,
consider a simple discretization strategy to pre-process them into binary features using the mean. For
example, a continuous feature x can be discretized using its mean as
![discrete_to_categorical](https://i.ibb.co/tKcjt8q/discrete-to-categorical.png)

![Problem 1 Analysis and Report](https://github.com/kapilgautamin/DecisionTree-Algorithm-Scratch/blob/master/report_problem1.pdf)


---------------------------------------------------------------------------------------------------------------

**Problem 2**: Implement Bagging and AdaBoost based on the decision tree code that you developed in previous problem.
This code has to be modified to work with ensemble methods.
- For this assignment, we will restrict ourselves to binary trees. This means that we will restrict ourselves
to two splits instead of multiple possible splits at each node. More precisely, each node is restricted to
be of the form xi = vk?, where it tests if the feature xi takes the value vk.
- Implement three functions: bagging(x, y, max depth, num trees), boosting(x, y, max depth,
num stumps) and predict example(x, h ens), where h ens is an ensemble of weighted hypotheses.
The ensemble is represented as an array of pairs [(alpha i, h i)], where each hypothesis and weight
are represented by the pair: (alpha i, h i).

**Data Sets**: We will use the Mushroom Data Set1 from the UCI Repository for this assignment. There are
22 attributes in this data set, of which we have dropped the attribute (stalk-root) as it contains too many
missing values. The data set has been converted from string to integer, with the unique feature values being
assigned indices starting from 0 in alphabetical order. Also note that rather than perform the classical task
of predicting whether the mushroom is poisonous or edible, our classification task is to predict (bruises?).
Experiments: Once you have debugged and tested your code, run the following experiments and write a
brief report answering the following questions:
- Construct four models for each combination of maximum depth d = 3; 5 and
bag size (k = 10; 20). Report the confusion matrix for these four settings.
- Construct four models for each combination of maximum depth d = 1; 2 and
bag size (k = 20; 40). Report the confusion matrix for these four settings.
- Use scikit-learn's bagging and AdaBoost learners and repeat the ex-
periments as described in parts (a) and (b) above. Report the confusion matrices for these sets of
settings. What can you say about the quality of your implementation's performance versus scikit's
performance?

![Problem 2 Analysis and Report](https://github.com/kapilgautamin/DecisionTree-Algorithm-Scratch/blob/master/report_problem2.pdf)
