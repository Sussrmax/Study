# 二分查找 和 二分答案
**二分答案**: 二分答案是一种用于求解 最优化问题 的策略， 通常用于“最大化最小值” 或 “最小值最大化” 的问题。

原理: 将可能解的范围进行二分，通过判断中间值是否满足问题条件来缩小搜索范围，直到找到最优解。<br>通常需要一个额外的验证函数来判断中间值的可行性。

二分查找: 数的范围(https://dashoj.com/p/88)
二分答案: 砍树(https://dashoj.com/p/89) ，分巧克力(https://www.luogu.com.cn/problem/P8647) 

二分答案的两题，整体形式和思路都大差不差，记录最大边界，二分来查找合适的结果
并无其他要说明的点