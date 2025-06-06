# 20点40分
---
## 函数指针
1. **函数指针** 指向的是 **函数** 而不是 **指针**，函数的类型由它的 **返回值类型** 和 **形参列表** 决定。
2. **函数重载** 只与**参数列表**有关，与**返回值**无关。
3. 当把**函数名**作为一个**值**使用时，**该函数自动转换为指针**，并且可以直接使用**指向函数的指针**调用函数就像普通的函数调用一般，而不需要对指针解引用
4. 对于**重载的函数**，编译器通过**指针类型**决定选用哪个重载函数。
5. **形参列表**不能定义**函数类型**的形参，但是可以定义**指向函数的指针**
6. **函数指针**之间不存在相互转化，但是可以给指针赋值为**0或者nullptr**，表示无指向。
7. 当对**函数**使用decltype时，返回的是**函数类型**而不是**函数指针**，需要我们显示声明 *。

---
## 关联容器
1. 关联容器共有 8 种，但是从整体上分为两类，一类是**map类型**，另一类是**set类型**, 从功能上分为三种，一种是有序不包含重复关键字的(map/set), 一种是无序的(unordered), 一种是包含重复关键字的(multi)。
2. 我们可以提供自己定义的操作来替代关键字上的 < 运算符，但所提供的操作必须在关键字类型上定义 严格弱序(小于等于)
如果一个类型定义了 “行为正常" 的 < 运算符，那么它可以用作关键字类型。
3. 未完待续
---
## 杂谈
从3.30 断commit 差不多有半个月了，摸鱼偷懒了差不多半个月，12号的时候去参加了蓝桥杯，人家学校真大，光是一个共享单车就是我们学校的一辈子(悲), 晚上没睡够加上死亡大巴，差点死车上。
比赛状况: 8道题只写出来了4道题，测试案例也就刚好通过，具体对多少道就不知道了，剩余4道只能说有思路，但时间不允许，估计只能那个三等奖了，吐槽一句，devc++是真的难用，我一个断点调试直接给程序干崩溃了，阿弥诺斯。
看了一下我的计划表，结合了一下我的行动力，只能说，心比天高，命比纸薄，也算是活该了，还得继续加油啊，时间紧，任务重
