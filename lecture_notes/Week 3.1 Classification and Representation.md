# Week 3.1 Classification and Representation
## Classification
![[classification1.png]]
+ Linear Regression is not a good idea

## Hypothesis Representation
### Sigmoid Function
+ we want $1 \le h_\theta(x) \le 1$
+ $g(\theta^T x)$
+ where $g(z) = \frac{1}{1 + e^{-z}}$ (**Sigmoid function/Logistic function**)
+ Our goal: fit parameters $\theta$ of our data
![[classification2.png]]
### Interpretation
+ $h_\theta (x)$: estimated probability that $y=1$ on input x
![[classification3.png]]
## Decision Boundary
+ predict $y=1$ when $z > 0$
+ predict $y=0$ when $z < 0$
+ Decision Boundary: the separate line
### Nonlinear Decision Boundary
![[classification5.png]]






