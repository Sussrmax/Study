# 17:37
## 算法题:  
* 回文数组 题目链接: https://www.luogu.com.cn/problem/P10902
* 挖矿 题目链接: https://www.luogu.com.cn/problem/P10904
* 比较字符串大小 题目链接: https://www.luogu.com.cn/problem/CF112A

## STL
* transform 和 for_each
* strcmp
### transform 和 for_each
可以对范围内的每个元素应用指定的操作，类似于for_each
但与for_each 不同的是，transform 专注于生成新值，将结果写入输出范围
返回尾后迭代器 

for_each: 
for_each 注重于执行副作用，比如打印元素，通常情况下不直接修改范围中的元素，除非在谓词中修改
for_each 返回 一元谓词 的副本

### strcmp
是C标准库中用来比较字符串大小的函数，逐个字符比较，直到碰到不同的元素或者到达字符串末尾('\0'); 区分大小写,接受C风格的字符串
相同返回 0
str1 > str2 返回 1
str1 < str2 返回 0