# 15:22

## 拷贝控制
1. **拷贝构造函数** 如果我们没有为一个类定义拷贝构造函数，编译器会为我们定义一个，其行为是调用对应 属性 的 拷贝构造函数(内置类型的成员则直接拷贝)
2. 直接初始化和拷贝初始化 <br> **直接初始化**: 要求编译器使用 普通的函数匹配 来选择与我们提供的参数最匹配的构造函数 <br> **拷贝初始化**: 要求编译器将 右侧运算对象 拷贝到正在创建的对象中，并在需要时进行类型转换(存在拷贝操作)
3. **拷贝赋值运算符** 和拷贝构造函数一样，如果类没有定义，那么编译器会给我们生成一个 合成拷贝赋值运算符
4. **析构函数** 注意: 引用和指针本身只是指向对象的工具，它们的存在或消失并不会直接影响它们所指向对象的生命周期
5. **=default** 使用 =default 告诉编译器生成 对应的 合成版本 <br> **注意**: 我们只能对 具有合成版本的成员函数 使用
6.  **=delete** 用来定义 删除的函数，定义了此函数可以阻止该函数被调用, 表明我们希望将某个函数定义为 删除的 <br> 与 =default 不同，=delete 可以作用于任何函数，但是不推荐作用于 析构函数 <br> 如果一个类有数据成员不能 默认构造，拷贝，复制或销毁，则对应的成员函数将被定义为删除的编译器会将这些合成的成员定义为 删除的函数
        
        
        
        
        
        
