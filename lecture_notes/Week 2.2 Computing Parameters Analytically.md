# Week 2.2 Computing Parameters Analytically
## Normal Equation
+ Normal equation: Method to solve for $\theta$ analytically
+ $\theta = (X^TX)^{-1}X^Ty$
[详解正规方程（Normal Equation](https://zhuanlan.zhihu.com/p/60719445)

```matlab
pinv (X'*X)*X'*y
```
+ X: design matrix
![[normal.png]]
+ Gradient Descent vs Normal Equation:
![[compare.png]]
## Normal Equation Noninvertibility
+ What if $X^TX$ is non-invertible? (rarely)
+ pinv: compute inverse even when invertible
+ Causes:
	+ Redundant features (linearly dependent)
	+ Too many feastures (e.g. $m \le n$)
		+ delete or use regularization
