# Data Types - Names Attribute

不止frame，所有R对象都可以有names属性

## names of vector
```R
> x <- 1:3
> names(x)
NULL
> names(x) <- c("foo","bar","norf")
> x
 foo  bar norf 
   1    2    3 
> names(x)
[1] "foo"  "bar"  "norf"
```

## names of list
```R
> x <- list(a=1, b=2, c=3)
> x
$a
[1] 1

$b
[1] 2

$c
[1] 3
```
## names of matrix
```R
> m  <- matrix(1:4, nrow=2, ncol=2)
> dimnames(m) <- list(c("a","b"),c("c","d"))
> m
  c d
a 1 3
b 2 4
```
list的中的第i个向量代表第i维的names，例如上面的list
```R
> list(c("a","b"),c("c","d"))
[[1]]
[1] "a" "b"

[[2]]
[1] "c" "d"
```
1、2个向量分别代表第1维（行）和第2维（列）的名字。


