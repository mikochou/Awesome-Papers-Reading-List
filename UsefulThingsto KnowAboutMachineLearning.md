# A Few Useful Things to Know About Machine Learning
https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf

一篇介绍一些关于ML的基础知识的文章，记一些感兴趣的点。

1. Overfitting:
* Cross-validation can help to combat overfitting
* adding a regularization term to the evaluation function

2. the curse of dimensionality:
* many algorithms that work fine in low dimensions become intractable when the input is highdimensional. （这个问题上次做推荐系统的时候遇到了，因为数据太大没有办法创建共现矩阵。）
* Learners can implicitly take advantage of this lower effective dimension, or algorithms for explicitly reducing the dimensionality can be used

3. Feature Engineering Is The Key:
features that look irrelevant in isolation may be relevant in combination. 

4. model ensembles
In boosting, training examples have weights, and these are varied so that each new classifier focuses on the examples the previous ones tended to get wrong. In stacking, the outputs of individual classifiers become the inputs of a “higher-level” learner that figures out how best to combine them.

