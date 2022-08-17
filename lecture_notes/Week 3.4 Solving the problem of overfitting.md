# Week 3.4 Solving the Problem of Overfitting
## The Problem of Overfitting
> **Overfitting:** If we have too many features, the learned hypothesis may fit the training set very well, but fail to generalize to new examples (predict prices on new examples).

![[overfitting.png]]
Options:
1. Reduce number of features
	+ Manually select which features to keep
	+ Model selection algorithm
2. Regularization
	+ Keep all the features, but reduce manitude/values of parameters $\theta_j$
	+ Works well when we have a lot of features, each of which contributes a bit to predicting $y$
## Cost Function
+ penalize parameters (small values)
![[penalize.png]]

+ what if $\lambda$ is too large: **results in underfitting**
## Regularized Linear Regression
+ For gradient descent, we repeat
+ $$
 \begin{array}
	 \\
	\theta_0 = \theta_0 - \alpha\frac{1}{m}\sum_{i=1}^{m}(h_\theta (x^{(i)}) - y^{(i)}x_0^{(i)})\\
	 \theta_j = \theta_j - \alpha[\frac{1}{m} \sum_{i=1}^{m}(h_\theta (x^{(i)}) - y^{(i)})x_j^{(i)} + \frac{\lambda}{m}\theta_j]
	 \\
 \end{array}
	 $$
+ We rewrite formula for $\theta_j$:
+ $$
\theta_j = \theta_j(1 - \alpha\frac{\lambda}{m}) - \alpha \frac{1}{m}\sum_{i=1}^{m}(h_\theta (x^{(i)}) - y^{x(i)})x_j^{(i)}
$$
+ $1 - \alpha\frac{\lambda}{m}$ is a bit smaller than 1

### Normal Equation Method
![[normal2.png]]
## Regularized Logistic Regression
$$
J(\theta) = -[\frac{1}{m}\sum_{i=1}^{m}y^{(i)}logh_\theta (x^{(i)}) + (1-y^{(i)})log(1-h_\theta (x^{(i)}))] + \frac{\lambda}{2m}\sum_{j=1}^{n}\theta_j^2
$$
+ Pseudocode:
+ ![[logistic_opt.png]]

+ [哲哲的ML笔记（十二：逻辑回归中的代价函数） - 简书 (jianshu.com)](https://www.jianshu.com/p/63c076b5b2be?u_atoken=3652618d-b8a8-4323-8d7f-f726eedcf5ae&u_asession=01N77A4CKWWRh-iDCCBOpxOuddZ0CVl_Rrc9dd2CwTQkPV6TbZWlZx2NtSC8k6jsIKX0KNBwm7Lovlpxjd_P_q4JsKWYrT3W_NKPr8w6oU7K9iws9CgWGHCDDid1KBxykIymCvuFU2gNCRIRJqGpb9omBkFo3NEHBv0PZUm6pbxQU&u_asig=05oKVigvANvKxFDWvrHXTSfAxc_ayXnHtuRe9K0nwH9LYabfY-boM0YJXNaAnfFbIWxgmGVwq92qpXMkPp7gYmnp5Dz5H2O3VpJxGvMESQuq55ufNc7iJGSioT5ckouMxYfedjKl161k3x8YiURZhQPFu-7gNYoKLoeZxGFe9YshD9JS7q8ZD7Xtz2Ly-b0kmuyAKRFSVJkkdwVUnyHAIJzbI6NNmkMukQI2gCacPS6jUcdELaX7Yfi10nScMcn7uBb4DvBakBj6x1SID70OM96u3h9VXwMyh6PgyDIVSG1W_2DM5fiIDXpm55UIy7-ihGT4NRbJBasC1DDxCNcnVYN3uC0i-CoWsF7WMRZ5ameVp6rTCgyhlz_X_BJWd0s2i_mWspDxyAEEo4kbsryBKb9Q&u_aref=J8kIrPq5j7mBLuJ9F2yS2MqGpWA%3D)
+ ![[logistic_cost4.png]]