# 23:11

## STL 算法
1. _if 版本的算法: 接受一个元素值的算法通常有_if 版本，接受一个 谓词 来替代 元素值
2. _copy 版本的算法: 一些重排算法会将重排后的元素写到原来的输入序列，_copy 版本会将重排后的元素写入到额外的目的空降
3. _copy_if 版本的算法: 接受一个 谓词 来替代 元素值，并将处理后的输入序列写入额外的目的空间，原来的不变

### 特定容器算法
由于 list 和 forward_list 的特殊性，因此它们有自己sort等算法
因为通用的 sort 要求迭代器拥有随机访问的能力，有此能力的有: vector, string, array, deque.
1. list.sort() 和 list.sort(camp)
2. reverse() 翻转元素
3. list1.merge(list2): 合并两个有序序列，并删除list2中的元素 <br> 而通用版本的 merge() 会将合并后的序列写入额外的目的空间，并不会删除
4. splice / splice_after(): 拼接两个序列，不要求顺序，同上。forward_list 会拼接到当前位置之后，list 会拼接到之前