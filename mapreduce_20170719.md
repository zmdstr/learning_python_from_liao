> MapReduce is a programming model and an associated implementation for processing and generating large data sets. Users specify a map function that processes a key/value pair to generate a set of intermediate key/value pairs, and a reduce function that merges all intermediate values associated with the same intermediate key. --Google

- map
map() 函数接收两个参数，一个是函数，一个是 Iterable，map 将传入的函数依次作用到序列的每个元素，并把结果作为新的 Iterator 返回。
- reduce  
reduce() 函数接收两个参数，一个是函数，一个是 Iterable，reduce 把结果继续和序列的下一个元素做累积计算。  
**map 映射 reduce 化简**  
- 推荐阅读  
[我是如何向老婆解释MapReduce的？](http://blog.jobbole.com/1321/)