# Container
* vector 等动态容器底层会设置一个阈值，当大于阈值时会进行一次扩容操作，并将容器中的所有元素拷贝到新空间中，并释放旧空间
* resize() 重新设置容器中元素个数
* capacity() 获取容器的容量
* shrink_to_fit() 会将 capacity 减少为 size 相同的大小
* string 对象中 substr() 可获取字符串， append() 类似于 emplace() , replace() 相当于 insert() 和 erase() 的结合
具体见 String.cpp