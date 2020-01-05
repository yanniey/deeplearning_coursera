A 5-course specialization by deeplearning.ai

1. Neural Networks and Deep Learning
	* Quiz
	* Programming Assignments

2. Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization
	* Quiz 
	* Programming Assignments

3. Structuring Machine Learning Projects
	Quiz and Programming Assignments

4. Convolutional Neural Networks
	Quiz and Programming Assignments

5. Sequence Models
	Quiz and Programming Assignments

Course 2 Week 1 
Regularization 
Regularization is a technique to reduce overfitting or variance by penalizing for complexity. We do that by adding a term to the loss function to penalize for large weights.


1. L2 Regularization
	* Apply Frobenius norm of a matrix which penalizes weight matrix from being too large
	* The bigger the lambda, the smaller the W matrix, and thus the less overfitting 
	* L2 Regularization vs. L1 Regularization
		* L1 regularization will make the W vector sparse (i.e. with lots of zeros)
	* lambda is the regularization parameter. The bigger the lambda, the smaller the weight will be - i.e. closer to 0(because SGD will work to reduce cost function)
	* The smaller the Frobenius norm, the less overfitting/ variance
	* L2 regularization is also called "weight decay" because it makes the matrix a little smaller (by multiplying the matrix by a number that's a little bit less than 1)

2. In general, the number of neurons in the previous layer gives us the number of columns of the weight matrix, and the number of neurons in the current layer gives us the number of rows in the weight matrix.


