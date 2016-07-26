# Data Types - Data Frames

在pandas里面用的够多了，强大复杂。

## Data Frame
- data frame用来存储表结构数据
- 是一种特殊的list，其每个元素都是list且所有元素的长度相等
- 它的一列可以看做它的一个元素，元素的长度则是frame的行数
- 不同于矩阵，frame可以存储不同类型的数据（不同列的类型可以不同）
- 特殊属性-rows.names，即每行有一个名字
- read.table()或read.csv()可以创建frame
- data.matrix()可将frame转为矩阵

## 实践
创建frame

```R
> x <- data.frame(foo=1:4,bar=c(T,T,F,F))
> x
  foo   bar
1   1  TRUE
2   2  TRUE
3   3 FALSE
4   4 FALSE
> nrow(x)
[1] 4
> ncol(x)
[1] 2
```

