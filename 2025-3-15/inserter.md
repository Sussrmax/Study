# 插入迭代器

* 插入迭代器通用的操作 <br> it = t 调用对应插入迭代器的容器的插入方法 <br>  *it / ++it / it-- 不会对迭代器做任何事，返回it, 同时意味着无法解引用

# back_inserter
* 创建一个使用 push_back 的迭代器，但需要容器支持操作 push_back, 插入元素后会将迭代器后移 <br> 类似:  c.push_back(), it++

# inserter
* 创建一个使用 insert 的迭代器, 同上

# front_inserter
* 创建一个使用 push_front 的迭代器, 同上