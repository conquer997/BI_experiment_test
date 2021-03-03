# 第二十一周作业——周日名企课

### Thinking1  电商定向广告和搜索广告有怎样的区别，算法模型是否有差别

1. 电商定向广告：用户没有很明显的意图；用户来到淘宝之前，自己也没有特别明确的目标。

   搜索广告：用户有明显的意图。

2. **算法模型有差别**

   定向广告推荐应用的典型模型是带Attention机制的DIN模型、DIEN模型和DSIN模型



### Thinking2  定向广告都有哪些常见的使用模型，包括Attention机制模型？

定向广告常见的使用模型有：LR模型，MLR模型，DNN模型，Deep Interest Network模型，Deep Interest Evolution Network模型，Deep Session Interest Network。



### Thinking3  DIN中的Attention机制思想和原理是怎样的?

1. **机制思想**

+ 在pooling的时候，与候选广告集相关的商品权重大一些，不相关的商品权重小一些；
+ 对用户兴趣的表示上引入了attention机制，对历史行为待征进行 embedding操作，视为对用户兴趣的表示，之后通过 Attention Unit，对每个兴趣表示赋予不同的权重。

2. **原理**

+ DIN 的基础模型 Base Model是一个典型的Embedding结构，它的输入特征有用户属性特征、用户行为特征、候选广告特征和场景特征；

+ 把ID特征转换成对应的 Embedding，然后把这些 Embedding 连接起来组成当前商品的 Embedding；

+ 通过SUM Pooling 层把带权重的商品的 Embedding 叠加起来，然后再把叠加后的 Embedding 跟其他所有特征的连接结果输入 MLP。



### Thinking4  DIEN相比于DIN有哪些创新?

1. 通过引入序列模型 AUGRU 模拟了用户兴趣进化的过程；
2. 在 Embedding layer 和 Concatenate layer 之间加入了生成兴趣的 Interest Extractor Layer 和模拟兴趣演化的 Interest Evolving layer；
3. 最终把当前时刻的“兴趣向量”输入上层的多层全连接网络，与其他特征一起进行最终的 CTR 预估



### Thinking5  DSIN关于Session的洞察是怎样的，如何对Session兴趣进行表达?

1. 使用带有Bias Encoding的Self-Attention机制→提取用户的Session兴趣向量；
2. 利用Bi-LSTM 对用户的Session之间的交互进行建模→带有上下文信息的Session兴趣向量；
3. 利用Activation Unit自适应地学习各种会话兴趣对目标item的影响。



### Thinking6  如果你来设计淘宝定向广告，会有哪些future work

​    使用好商品的使用周期，利用用户复购商品的平均周期，作为该商品的寿命周期，用户下单后短期内不推荐该类商品。

​    对数据进行缺失值填充，数据异常值处理，数据格式处理，根据各个变量，制定不同维度的变量计算，反映更多的数据信息。