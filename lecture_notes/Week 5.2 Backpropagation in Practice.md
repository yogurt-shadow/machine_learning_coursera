# Week 5.2 Backpropagation in Practice
## Unrolling Parameters
+ unroll a matrix into a big long vector
![[unroll.png]]
## Gradient Checking
+ two-side difference:
$$\frac{d}{d\theta}J(\theta) \approx \frac{J(\theta+\epsilon) - J(\theta-\epsilon)}{2\epsilon}
$$
+ one-side difference:
$$
\frac{d}{d\theta}J(\theta) \approx \frac{J(\theta+\epsilon)-J(\theta)}{\epsilon}
$$
+ check $gradApprox \approx Dvec$
## Random Initialization (Symmetry breaking)

+ Initialize $\Theta_{ij}^{(l)}$ to a random value in $[-\epsilon, \epsilon]$
## Putting it Together
**Training a Neural Network**

1.  Randomly initialize the weights
    
2.  Implement forward propagation to get hΘ(x(i)) for any x(i)
    
3.  Implement the cost function
    
4.  Implement backpropagation to compute partial derivatives
    
5.  Use gradient checking to confirm that your backpropagation works. Then disable gradient checking.
    
6.  Use gradient descent or a built-in optimization function to minimize the cost function with the weights in theta

