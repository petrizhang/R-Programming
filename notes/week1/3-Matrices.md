# Data Types - Matrices

## 矩阵
矩阵是有维度属性的向量，维度属性是一个两元素的向量(nrow, ncol),
描述矩阵的行数和列数。

## matrix()
使用matrix函数可以创建一个矩阵，元素缺省值为`NA`

```R
> m <- matrix(nrow=2, ncol=3)
> m
     [,1] [,2] [,3]
[1,]   NA   NA   NA
[2,]   NA   NA   NA
> dim(m)
[1] 2 3
> attributes(m)
$dim
[1] 2 3
``

## 使用向量初始化矩阵
与MALATB相同，R中的矩阵存储以列为主序
```R
> m <- matrix(1:6, nrow=2, ncol=3)
> m
     [,1] [,2] [,3]
[1,]    1    3    5
[2,]    2    4    6
```

## 通过改变向量的dim属性创建矩阵
```R
> m <- 1:10
> m
 [1]  1  2  3  4  5  6  7  8  9 10
> dim(m) <- c(2,5)
> m
     [,1] [,2] [,3] [,4] [,5]
[1,]    1    3    5    7    9
[2,]    2    4    6    8   10
```

## cbind() 和 rbind()
通过column-binding或row-binding也可以创建矩阵
```R
> x <- 1:3
> y <- 10:12
> cbind(x,y)
     x  y
[1,] 1 10
[2,] 2 11
[3,] 3 12
> rbind(x,y)
  [,1] [,2] [,3]
x    1    2    3
y   10   11   12
```
