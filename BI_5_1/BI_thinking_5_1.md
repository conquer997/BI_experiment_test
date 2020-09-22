# 第五周作业——周二核心课

## Thinking 1   在实际工作中，FM和MF哪个应用的更多，为什么

1. 实际工作中，MF应用更多。
2. MF只有user, item两个特征，而FM有多个特征



## Thinking 2   FFM与FM有哪些区别？

1. FM算法中，每个特征对应一个隐向量
2. FFM算法是FM算法的改进，引入了field的概念，每个特征有f-1个隐向量



## Thinking 3   DeepFM相比于FM解决了哪些问题，原理是怎样的

1. 首先，使用FM Component + Deep Component。
2. FM提取低阶组合特征，Deep提取高阶组合特征。
3. DeepFM是端到端的训练，不需要人工特征工程，和Wide&Deep不同。
4. 其次，共享feature embedding。FM和Deep共享输入和feature embedding不但使得训练更快，而且使得训练更加准确。
5. 



## thinking 4   Surprise工具中的baseline算法原理是怎样的？BaselineOnly和KNNBaseline有什么区别？

1. Baseline算法：基于统计的基准预测线打分
2. BaselineOnly：给定用户和Item，给出基于baseline的估计值
3. KNNBaseline：考虑基线评级的协同过滤



## Thinking 5   基于邻域的协同过滤都有哪些算法，请简述原理

4. KNNBasic：最基础的K近邻协同协同
2. KNNWithMeans：将每个用户评分均值考虑在内的协同过滤
3. KNNWithZScore：协同过滤算法的变种，考虑每个用户评分的归一化操作
4. KNNBaseline：协同过滤算法的变种，考虑每个用户评分的基线