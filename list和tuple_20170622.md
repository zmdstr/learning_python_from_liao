- list 列表
list 是一种**有序**的集合，可以随时添加和删除其中的元素。
```python
classmates = ['Michael', 'Bob', 'Tracy']
```  
- list 的索引从 0 开始
- 可以用 -1 做索引，直接获取最后一个元素  
- 相关操作
```python
append #追加
insert #插入
pop #删除
```

list 里面的元素的数据类型也可以不同   
list 元素也可以是另一个 list  

- tuple 元组
tuple 和 list 非常类似，也是有序的，但是 tuple **一旦初始化就不能修改**  
```python
classmates = ('Michael', 'Bob', 'Tracy')
```
> 不可变的 tuple 有什么意义？因为 tuple 不可变，所以代码更安全。如果可能，能用tuple 代替 list 就尽量用 tuple。  
- 看一个“可变的” tuple  
```python
>>> t = ('a', 'b', ['A', 'B'])
>>> t[2][0] = 'X'
>>> t[2][1] = 'Y'
>>> t
('a', 'b', ['X', 'Y'])
```
> 表面上看，tuple 的元素确实变了，但其实变的不是 tuple 的元素，而是 list 的元素。tuple 一开始指向的 list 并没有改成别的 list，所以，tuple 所谓的“不变”是说，tuple 的每个元素，指向永远不变。即指向 'a'，就不能改成指向 'b'，指向一个 list，就不能改成指向其他对象，但指向的这个 list 本身是可变的！
总结：  
list 和 tuple 是 Python 内置的有序集合，一个可变，一个不可变。根据需要来选择使用它们。


