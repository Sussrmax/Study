# 20:50

## 算法题:
代码见: LQB_Preparing for competition\Test.cpp
### Registration System 
题目链接: https://www.luogu.com.cn/problem/CF4C

整体思路: 通过一个哈希表来记录每个字符串，如果第一次碰到则输出"OK" 并将 字符串对应的哈希表中的值加一，如果重复碰到则用字符串 拼接 哈希表中的值

### Plug-in
题目链接: https://www.luogu.com.cn/problem/CF81A

整体思路: 题目的要求是删除 重复的 连续的 字符对, 那么通过一个栈来解决，维护栈顶元素，第一次碰到则入栈，如果 s[i] 与栈顶元素相同的话则 栈顶出栈并跳过 s[i]

### Boxes Packing
题目链接: https://www.luogu.com.cn/problem/CF903C

整体思路: 双指针，先对元素进行排序，左指针指向第一个元素，右指针开始移动，如果碰到大于左指针指向的元素，意味着可以将其放入当前盒子中，否则右指针继续移动，最终通过计算法左右指针的范围得出结果