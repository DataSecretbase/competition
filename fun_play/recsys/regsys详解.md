>  文本中使用了数学公式 需要支持latex的编辑器打开如typora    或在网页中引入MathJax.js)



在 Surprise包里

支持的算法包有

| 算法            |         |
| ------------- | ------- |
| SVD           | 奇异值分解   |
| SVD++         | 奇异值分解++ |
| NMF           | 非负矩阵分解  |
| Slope One     | 斜坡算法    |
| k-NN          | 最近邻算法   |
| Centered k-NN | 居中最近邻算法 |
| k-NN Baseline |         |
| Co-Clustering | 协同聚类算法  |
| Baseline      |         |
| Random        |         |
|               |         |
|               |         |
|               |         |
|               |         |





##Slope One算法

基于不同物品之间的评分差的线性算法，预测用户对物品评分的个性化算法。主要两步： 

Step1:计算物品之间的评分差的均值，记为物品间的评分偏差(两物品同时被评分)； 

$R(ij)=\frac{\sum\limits_{u\in N(i) \cap N(j)} (r_{ui}-r_{uj})}{|N(i) \cap N(j)|}$ 

其中，$r(ui)$ 是用户u对物品i的评分，$r(uj)$ 是用户u对物品j的评分。$N(i)$是对物品评分过的用户，而$N(i)\cap N(j)$ 是对物品i和物品j都评过分的用户，$|N(i)\cap N(j)|$ 是对物品i和物品j都评过分的用户。