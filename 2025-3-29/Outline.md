# 19:32

## 位掩码
位掩码本质上就是一个特殊的二进制码。
通过位移运算符生成特定的二进制码来解决问题
位操作: <<, >>, |, &, ^, ~

常见操作: 
* 检查特定位：用 & 检查某位是否为1。
* 设置特定位为1：用 | 将某位设为1。
* 清除特定位为0：用 & ~ 将某位清为0。
* 翻转特定位：用 ^ 翻转某位的值。

## 算法题
**穿越时空之门**
题目链接: https://www.lanqiao.cn/problems/19701/learning/
二进制转四进制

**握手问题**
题目链接: https://www.lanqiao.cn/problems/19695/learning/
整体思路: 第一个人握49次，第二个人握48次，依次类推，到第43个人时应该握6次，但是有7个人之间互不握手，那么从43开始就不继续累加了

**一维前缀和**
题目链接: https://www.lanqiao.cn/problems/18437/learning/


**二位前缀和**
题目链接: https://www.lanqiao.cn/problems/18439/learning/

**一维差分**
题目链接: https://www.lanqiao.cn/problems/18438/learning/

**二维差分**
题目链接: https://www.lanqiao.cn/problems/18440/learning/

原数组: A， 差分数组: D
差分公式: D[i, j] = A[i][j] - A[i - 1][j] - A[i][j - 1] + A[i - 1][j - 1];

公式是如何得来的?
二维差分数组的一个目标: 通过前缀和可以还原成原数组，通过该目标可推断出该公式

*注*: 代码示例见: LQB_Preparing for competition\Test_2.cpp