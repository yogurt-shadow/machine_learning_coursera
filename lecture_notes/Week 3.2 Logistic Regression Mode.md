# Week 3.2 Logistic Regression Mode
## Cost Function
+ convex problem about logistic regression when we use linear regression's cost function
![[convex.png]]
+ **Cost function of logistic regression**
+ $$
Cost(h_\theta (x), y) = \begin{cases}
-log(h_\theta (x)) & y=1 \\
-log(1 - h_\theta (x)) & y = 0
\end{cases}
$$
![[logistic_cost1.png]]
![[logistic_cost2.png]]
## Simplified Cost Function and Gradient Descent
+ simplified cost function:
+ $$Cost(h_\theta (x), y) = -ylog(h_\theta (x)) - (1 - y)log(1 - h_\theta (x))$$
+ Entire cost function:
+ $$J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} [y^{(i)}log(h_\theta (x^{(i)})) + (1 - y^{(i)})log(1 - h_\theta (x^{(i)}))]$$
![[logistic_cost3.png]]
## Advanved Optimization
Suppose we want to $min_\theta J(\theta)$
we have code to calculate $J(\theta)$ and $\frac{\partial}{\partial(\theta_j)} J(\theta)$

Optimization Algorithm:
- Gradient descent
- Conjugate gradient
- BFGS
- L-BFGS

+ Advantages:
	1. no need to manually pick $\alpha$
	2. often faster than gradient descent
+ Disadvantages:
	+ More complex

+ Code in Octave:
![[octave1.png]]






