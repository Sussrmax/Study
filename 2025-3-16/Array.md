# 数组名的退化

## 一维数组名
在一些情况下数组名会转化为指向第一个元素的指针，如 fill(arr, arr + n, n);
有时候却不会发生转换: 如 用sizeof 计算所占内存空间 arr 表示一整个数组

## 二维数组名
在一些情况下二维数组名会转化为 指向第一行数组的指针(数组指针, int *[n]), 因此对二维数组使用 fill(arr, arr + n * n , n) 时会报错，应将arr 改为 &arr[0][0];
虽然 arr 和 &arr[0][0] 在内容上相同，但是在类型上是不同的，arr 是 int *[n] 类型 而 &arr[0][0] 是 int * 类型
arr 指向第一行，从第一行的角度出发，arr 是一个一维数组，而数组名 表示的是第一个元素的地址，因此两者在数值上是相同的
如果函数参数中包含(void * ) 则可以将二维数组名直接作为参数传递。
