>*“写于 2017-06-22 
重新整理笔记结构 2017-07-09”*

## list 列表
list 是一种**有序**的集合

#### 1.定义一个 list 
```python
#1.定义一个有元素的 list
classmates = ['Michael', 'Bob', 'Tracy']
#2.定义一个空的 list
L = []
```  
#### 2.操作 list 
- 增
```python
#1.追加
>>> names = []
>>> names.append('kaer')
>>> names
['kaer']
#2.指定位置插入
>>> names.insert(0,'huonv')
>>> names
['huonv', 'kaer']
```
- 删
```python
#1.删除最后一个元素，返回被删除元素
>>> names.pop()
'kaer'
>>> names
['huonv']
#1.删除指定位置元素
>>> names.pop(0)
'huonv'
>>> names
[]
```
- 改
```python
>>> names=['fengxingzhe','xiaoxiao']
>>> names[0]='shengqishi'
>>> names
['shengqishi', 'xiaoxiao']
```
- 查
```python
#1.查看整个所有 list 元素
>>> names
['shengqishi', 'xiaoxiao']
#2.查看指定位置元素
>>> names[0]
'shengqishi'
#3.查看最后一个元素
>>> names[-1]
'xiaoxiao'
#4.查看 list 长度
>>> len(names)
2
```

#### 3.说明
- list 的索引从 0 开始
- 可以用 -1 做索引，直接获取最后一个元素  
- list 里面的元素的数据类型也可以不同   
- list 元素也可以是另一个 list  

## tuple 元组
tuple 和 list 非常类似，也是有序的，但是 tuple **一旦初始化就不能修改**，因此 tuple 操作只有查，方法同 list  
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

## 总结  
list 和 tuple 是 Python 内置的有序集合，一个可变，一个不可变，注意他们的定义方式，一个 [] ，一个 ()。由于 python 是动态类型语言，在定义变量时，不会显示声明变量类型，因此你要条件反射的看到 [] 想到 list，看到 ()，想到 tuple。