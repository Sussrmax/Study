# 21点03分
* LCA
* 倍增算法
* 邻接表
* 邻接矩阵
---
## 邻接表和邻接矩阵
**邻接矩阵**: 通过一个n x n二维的数组记录边，横竖的 n 均表示元素序列 <br> 两点之间有边，那么对应的 arr[i][j] 和 arr[j][i] 为 1，无边为 0
**邻接表**: 有两种记录方式
* 第一种: 哈希表+链表(/动态数组), key 为节点的序列，value 为节点序列所连的节点构成的列表(推荐使用)
* 第二种: 通过在定义一个存有当前索引的节点以及相连的节点索引的数据结构和一个节点序列head;代码如下: <br> struct node { int node, next_index; }; node E[N]; <br> int head[N]; 查找方式: 通过 head[i] 存有对应 E中的索引下标， E[head[i]] 找到第一个相连节点，通过 E[head[i]].next_index 找到下一个与 i 相连的节点，详细见: G_1.cpp
---
## 倍增算法
倍增法中，我们不只记录每个节点的直接父节点(1步祖先), 还记录它跳 2^0 = 1步， 2^1 = 2步， 2^2 = 4步等祖先
通过记录 2^k 步的祖先，可以用这些“跳跃距离” 组合出任意步数的向上移动。
例如: 想跳7步，可以用 4 + 2 + 1(即 2^2 + 2^1 + 2^0)来完成该操作

---
# LCA
最近公共祖先(LCA), 常用倍增算法来实现LCA 的查找