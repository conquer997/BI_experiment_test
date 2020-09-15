# 第四周作业——周二核心课



## Thinking 1   ALS都有哪些应用场景

交替最小二乘法，在机器学习中，ALS特指使用最小二乘法求解的一个协同过滤算法，是协同过滤中的一种。应用场景即有推荐系统，如现在比较火的视频推荐，购物推荐，商品推荐等。



## Thinking 2	ALS进行矩阵分解的时候，为什么可以并行化处理

因为ALS在进行矩阵分解的时候，本质是矩阵运算，矩阵元素直接没有相互依赖性，因此可以实现并行化处理



## Thinking 3	梯度下降法中的批量梯度下降（BGD），随机梯度下降（SGD），和小批量梯度下降有什么区别（MBGD）

1. **批量梯度下降法**是最原始的形式，它是指在**每一次迭代时**使用**所有样本**来进行梯度的更新。
2. **随机梯度下降法**不同于批量梯度下降，随机梯度下降是**每次迭代**使用**一个样本**来对参数进行更新。使得训练速度加快。
3. **小批量梯度下降**，是对批量梯度下降以及随机梯度下降的一个折中办法。其思想是：**每次迭代** 使用 **batch_size** 个样本来对参数进行更新。



## Thinking 4	你阅读过和推荐系统/计算广告/预测相关的论文么？有哪些论文是你比较推荐的，可以分享到微信群中

1. 协同过滤第一次提出：Using collaborative filtering to weave an information Tapestry. David Goldberg

2. 基于内容的推荐：Content-Based Recommendation Systems. Michael J. Pazzani and Daniel Billsus

3. 推荐冷启动的论文：Addressing Cold-Start Problem in Recommendation Systems. Xuan Nhat Lam.etl