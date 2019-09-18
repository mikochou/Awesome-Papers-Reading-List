# A comparative study of decision tree ID3 and C4.5
 [https://saiconference.com/Downloads/SpecialIssueNo10/Paper_3-A_comparative_study_of_decision_tree_ID3_and_C4.5.pdf](https://saiconference.com/Downloads/SpecialIssueNo10/Paper_3-A_comparative_study_of_decision_tree_ID3_and_C4.5.pdf) 

This paper mainly introduces the decision tree algorithm ID3 and C4.5 and compare them.

### ID3 algorithm:
Entropy is basically a measure of uncertainty
定义：
`entropy(X) = -∑pilog2pi`
p_i是i在数据集中出现的概率。
例如，一个数据集中含有60个items，第一个item出现14次，第二个item出现27次，第三个出现19次，那么信息熵为：
`entropy = - (14/60)*log(14/60) - (27/60)*log(27/60) - (19/60)log(19/60) = 1.537`
如果使用决策树，如下：
```
left subtree = [5, 21, 11]
right subtree = [9, 6, 8]
```
信息熵如下：
```
left entropy = - (5/37)log(5/37) - (21/37)log(21/37) - (11/37)log(11/37) = 1.374
right entropy = - (9/23)log(9/23) - (6/23)log(6/23) - (8/23)log(8/23) = 1.565
overall entropy = (37/60)*1.374 + (23/60)*1.565 = 1.447
```
可以看出，信息熵变少了，信息增益（information gain）则是指这个过程中熵的变化。
`information gain = 1.537 - 1.447 = 0.09`

### C4.5 algorithm: 
limitation in ID3: overly sensitive to feature with large numbers of values
C4.5 uses Gain ratio:
![](https://tva1.sinaimg.cn/large/006y8mN6gy1g73kb203t6j319w0t8jyw.jpg)
* A possibility to use continuous data. 
* Using unknown (missing) values 
* Ability to use attributes with different weights. 
* Pruning the tree after being created.

### Experiment
在不同大小的dataset上实验，准确度和效率C4.5都高于ID3
