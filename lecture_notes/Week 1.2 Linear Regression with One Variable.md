# Week 1.2 Linear Regression with One Variable
## Model Representation
+ Notation:
	+ m: Number of training examples
	+ x's: "input" variable/features
	+ y's: "output" variable/"target" variable
	+ (x, y) one training example
	+ $(x^i, y^i)$ i-th training example
![[linear_regression.png]]
## Cost Function
+ Hypothesis: $h_\theta(x) = \theta_0 + \theta_1x$
+ Parameters: $\theta_i's$
+ Idea: Choose $\theta_0, \theta_1$ so that $h_\theta(x)$ is close to $y$ for our training examples $(x, y)$
+ Cost Function (squared error function):
$$J(\theta_0, \theta_1) = \frac{1}{2m}\sum_{i=1}^m (h_\theta(x^{(i)})-y^{(i)})^2$$
![[linear_regression2.png]]

