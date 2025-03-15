# bind

*  位于头文件 function 中
*  bind 函数可以视为一个函数适配器，生成一个新的可调用对象来"适应" 原对象的参数列表
*  例如一些算法接受一元谓词，当我们想要使用我们的函数(或者叫可调用对象) 来替换谓词时发现可能会有些困难, 例如: 我们想通过 find_if 查找字符串长度大于 n  的字符, 在通常情况下我们定义的函数为了保证通用性会让调用者传入两个参数，一个是字符串，一个是长度 n : check(string & str, int n) ; <br> 我们想使用该函数作为 find_if 的谓词，但是 check 是一个 二元谓词，因此不符合要求。使用 bind() 可解决 <br> auto check_5 = bind(check, _1, 5); 这样就可以将 check_5 作为谓词传递给 find_if
*  格式: auto newCallable = bind(callable,  arg_list);
*  其中 arg_list 包含 _n 的名字(如上面的  _1) 表示占位符，想要使用这些占位符需要单独的声明. 如: using namespace placeholders; / using std::placeholders::_n;
*  _n 这些名字也有先后顺序，例如 _1 表示第一个接受的参数。通过设置不同顺序的 _n 可以达到不同的效果，详细见 GQ_2.cpp
*  bind 对参数的操作通常是拷贝，需要引用的话需要我们使用 function 中定义的函数 ref() / cref() :  返回一个对象，包含给定对象的引用
