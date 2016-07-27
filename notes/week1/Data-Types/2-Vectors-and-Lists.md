# Data Types - Vectors and Lists

## 创建Vector

### c()
c()函数可以创建向量，c为concatenate的简写
```R
x <- c(0.5, 0.5)     ##numeric
x <- c(TRUE, FALSE)  ##logical
x <- c(T, F)         ##logical
x <- c("a","b","c")  ##character
x <- 9:29            ##integer
x <- c(1+0i, 2+4i)   ##complex
```

### vector()
```R
x <- vector("numeric", length=10)
```
x的元素会有默认值0

## 使用不同类型元素创建vector

使用c()连接不同类型的元素时，R会进行隐式的强制转换，将所有元素转为合适的同一类型
```R
y <- c(1.7, "a")    ##character
y <- c(TRUE, 2)     ##numeric
y <- c("a", TRUE)   ##charater
```

## Explicit Coercion
### 使用as.*进行强制类型转换
```R
> x <- 0:6
> class(x)
[1] "integer"
```
对x进行各转换的结果：
```R
> as.numeric(x)
[1] 0 1 2 3 4 5 6
> as.logical(x)
[1] FALSE  TRUE  TRUE  TRUE  TRUE  TRUE  TRUE
> as.character(x)
[1] "0" "1" "2" "3" "4" "5" "6"
```
### 非法转换
若不能转换成指定类型，将得到`NA`值并产生警告
```R
> x <- c("a","b","c")
> as.numeric(x)
[1] NA NA NA
Warning message:
强制改变过程中产生了NA 
> as.logical(x)
[1] NA NA NA
> as.complex(x)
[1] NA NA NA
Warning message:
强制改变过程中产生了NA
```

## list
list的元素可以为不同类型
```R
> x <- list(1,"a",T, 1 + 4i)
> x
[[1]]
[1] 1

[[2]]
[1] "a"

[[3]]
[1] TRUE

[[4]]
[1] 1+4i
```



