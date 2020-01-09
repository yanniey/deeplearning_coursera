A 5-course specialization by deeplearning.ai

1. Neural Networks and Deep Learning
	* Quiz
	* Programming Assignments

2. Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization
	* Quiz 
	* Programming Assignments
		* Week 1: Initialization (Zeros, Random & He), regularization, gradient checking
		* He initialization works well for networks with ReLU activations.

3. Structuring Machine Learning Projects
	Quiz and Programming Assignments

4. Convolutional Neural Networks
	Quiz and Programming Assignments

5. Sequence Models
	Quiz and Programming Assignments



====== 
Course 2 

Week 1 
Regularization 
	* Regularization is a technique to reduce overfitting or variance by penalizing for complexity. We do that by adding a term to the loss function to penalize for large weights.


1. L2 Regularization
	* Apply Frobenius norm of a matrix which penalizes weight matrix from being too large

	* The bigger the lambda, the smaller the W matrix, and thus the less overfitting 

	* L2 Regularization vs. L1 Regularization
		* L1 regularization will make the W vector sparse (i.e. with lots of zeros)

	* lambda is the regularization parameter. The bigger the lambda, the smaller the weight will be - i.e. closer to 0(because SGD will work to reduce cost function)

	* The smaller the Frobenius norm, the less overfitting/ variance

	* L2 regularization is also called "weight decay" because it makes the matrix a little smaller (by multiplying the matrix by a number that's a little bit less than 1)

2. In general, the number of neurons in the previous layer gives us the number of columns of the weight matrix, and the number of neurons in the current layer gives us the number of rows in the weight matrix.

3. Other methods of regularization
	* data augmentation: e.g. flipping the image horizontally, zooming in a random part of the image
	* early stopping

Gradient checking
1. Don't use in training - we should only use it to debug
2. Gradient checking doesn't work with dropout (due to the randomness), so we should turn off dropout (e.g. using `keep-prob = 1`)





* Make sure dev and test sets have the same distribution
* When the data set is big, 98% training / 1% dev / 1% testing
* Not having a test set might be okay (only dev set)


High bias? (training data perform worse than dev data)
	* Bigger network / more layers / more hidden units
	* train for longer / more iterations
	* search for a better neural network architecture for the problem

Once we solve the high bias (i.e. underfitting problem), we can move to the High Variance? problem by looking at performance of the dev set

Is the dev set performance in line with training set performance?
Solutions:
	* More data
	* Regularization
	* Search for a better neural network architecture for the problem


======


Week 2
Optimization algorithms
	* Gradient descent, mini-batch & SGD
	* Exponentially weighted averages (EWMA)
	* Gradient descent with momentum
	* RMSprop (Root mean square prop)
	* Adam optimisation (Adaptive Moment Estimation)

1. Mini-batch gradient descent
How to choose batch size? 
	* If small dataset (i.e. training sample size m <= 2000), just use batch gradient descent
	* Otherwise, typical batch sizes are 64, 128, 256 to 512
	* Note: make sure that mini batch sizes fit into CPU/GPU memory

2. Exponentially weighted averages
	* Beta (a value between 0 and 1) determines moving average over the past x days. 
	* The closer beta is to 1, the longer a period the moving average covers, which results in a smoother curve
	* The closer beta is to 0, the more noisy / overfitting the curve would be as it will respond to short term changes more quickly

3. Bias correction: corrects bias in the initial observations 

4. Momentum
	* Compute an exponentially weighted average of the gradients, and then use that gradient to update the weights instead
	* Generally faster than gradient descent without momentum

5. RMSprop 
	* Also speeds up gradient descent by allowing for a larger learning rate & reducing oscilations in mini batch descent

6. Adam 
	* Combines RMSprop and momentum








