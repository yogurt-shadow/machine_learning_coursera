# Week 1.3 Parameter Learning
## Gradient Descent
1. Start with some $\theta_0, \theta_1$
2. Keep changing $\theta_0, \theta_1$ to reduce $J(\theta_0, \theta_1)$ until we hopefully end up at a minimum
+ repeat until convergence {
$$
\theta_j := \theta_j - \alpha\frac{\partial}{\partial\theta_j}J(\theta_0, \theta_1)	
$$
} for ($j = 0$ and $j = 1$)
+ $\alpha$: learning rate
+ Simultaneously: update $\theta_0$ and $\theta_1$
+ Intuition:
![[gradient1.png]]
## Intuition
+ too small
> if $\alpha$ is too small, gradient descent can be slow
+ too large:
> if $\alpha$ is too large, gradient descent can overshoot minimum. It may fail to converge, or even diverge.
+ Gradient descent can converge to a local minimum, even with the learning rate $\alpha$ fixed
> As we approach a local minimum, gradient descent will automatically take smaller steps. So, no need to decrease $\alpha$ over time.

![[gradient2.png]]
## Gradient Descent for Linear Regression
$$
\frac{\partial}{\partial\theta_0}J(\theta_0, \theta_1) = \frac{1}{m}\sum_{i=1}^{m}(h_\theta(x^{(i)}) - y^{(i)})
$$
$$
\frac{\partial}{\partial\theta_1}J(\theta_0, \theta_1) = \frac{1}{m}\sum_{i=1}^{m}(h_\theta(x^{(i)}) - y^{(i)})x^{(i)}
$$
+ "convex function": bowl-shaped, only one global optimum
+ "Batch" Gradient Descent: each step of gradient descent uses all the training examples
