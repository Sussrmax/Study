# 记录时间: 21:17

## 继承

### 抽象基类
如果一个类中含有一个或多个 **纯虚函数**，则该类是一个抽象基类，**不能被示例化**，**后续的派生类必须实现所有的纯虚函数，否则该类也是一个抽象基类**

**纯虚函数**:
纯虚函数是在基类中声明的函数，**没有类内实现**，**只能通过类外实现**(如果后续需要调用基类的纯虚函数的话)
<br>声明格式是在 函数声明的末尾加上 =0, 例如: virtual void Func() = 0;

派生类构造函数只初始化它的直接基类
        
### 友元与继承
**友元关系不能继承**, 每个类负责控制各自成员的访问权限
**基类的友元在访问 派生类成员 时不具有特殊性**， 派生类的友元 **也不能随意访问** 基类的成员

**改变成员的可访问性**
通过 **using 声明** 可以达到改变 某个成员的访问级别，所改变的级别通常与原来的相同
可以对该类的 **直接或间接基类** 中的任何可访问成员使用 using
        
### 继承中的类作用域
**派生类的作用域嵌套在其基类的作用域内**

当出现同名的成员时，派生类会**隐藏父类**的成员(即内层作用域隐藏外层作用域)

声明在内层作用域的函数不会重载声明在外层作用域的函数，因此如果出现同名的函数时会隐藏外层的 

**覆盖重载的函数**
通常情况下如果派生类出现与基类同名的函数时会隐藏基类中的同名函数(包括重载)，此时通过使用using 加上 函数名 便可解决这个问题

### 构造函数与拷贝控制
**虚析构函数**
如果 **基类的析构函数** 不是 虚函数，**则delete 一个指向派生类对象的基类指针 将产生未定义的行为**

**移动操作与继承**
虚析构函数将**阻止**编译器为我们提供合成的移动操作，除非显示定义(使用 =default)

默认情况下，基类不含有合成的额移动操作(因为基类一般都会定义基类的虚析构函数), 且由于基类缺少移动操作会阻止派生类拥有自己的合成移动操作
所有当我们确定**需要为一个类定义移动操作时，则需要我们在其基类中进行定义**, 有了移动操作，那么需要我们同时提供拷贝操作

**在默认情况下，基类默认构造函数初始化派生类对象的基类部分**。如果我们想拷贝(或移动)基类部分，则必须在派生类中对应的函数中显示调用基类对应的函数，例如: 在派生类赋值运算符函数体中显示调用基类的赋值运算符，在派生类构造函数列表后使用基类构造函数 

### 关于move 的补充
move 会将 **原目标** 转换成一个右值引用，**表示希望以"移动"的方式使用它，然而是否执行移动操作，取决于目标类是否提供了移动操作，如果没有移动操作，那么move 的调用会退化为使用拷贝操作**

## 算法题
2025蓝桥杯省Bc++组
题目:
产值调整
题目链接: https://www.luogu.com.cn/problem/P12133

移动距离
题目链接: https://www.luogu.com.cn/problem/P12130

生产车间
题目链接: https://www.luogu.com.cn/problem/P12136

画展布置
题目链接: https://www.luogu.com.cn/problem/P12134
