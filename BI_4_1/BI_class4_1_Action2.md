# 第四周作业——周二核心课

# Action 2

## Slope One Predictors for Online Rating-Based Collaborative Filtering



**一、摘要：**

1. slope-one是一种item-based的协同过滤算法，核心思想是线性回归f(x) = x+b

2. 根据用户对item的评分信息，得到任意两个item之间的回归直线。然后根据已评分item计算未评分item的分值。最后根据计算出来的item的分值排序做推荐

3. 它的优点是算法简单，容易实现，可扩展性也不错，但需要是基于评分的，如果没有评分，需要构造评分

**二、相关研究**

1.  memory-based和model-based CF

**三、CF方案**

1. Per User Average

2. 基于Pearson相关度的算法，user-based CF

3. 基础的slope-one算法

4. 带权的slope-one算法

5. bi-polar  slope one算法

**四、实验结果**

1. 测试使用EachMovie和MovieLens数据集，MAE评估推荐质量，并比较了Bi-polar slope one, weighted slope one, slope one, bias from mean等算法，对于EachMovie数据集，Pearson和Bi-polar slope one的表现最佳。

2. 对于MovieLens数据集，三种slope-one算法表现同样好，并且优于所有其他算法。



**五、个人想法**

Slope one推荐算法流行，有一定优势：

1. 实现简单并且易于维护。

2. 响应即时，并且用户的新增评分对推荐数据的改变量较小。