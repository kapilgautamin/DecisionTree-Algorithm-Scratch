**Problem**: Implement a fixed-depth decision tree algorithm, that is, the input to the ID3 algorithm
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
