# Data Types - Factors

## Factors
Factors用来表示分类数据，可以是有序的也可以是无序的。
- factor可以看作一个整数向量，其中每个整数都有一个标签
- factor被lm()、glm()等建模函数特殊对待
- 可以看做枚举组成的向量

## R代码
创建一个factor:
```R
> x <- factor(c("yes","yes","no","yes","no"))
> x
[1] yes yes no  yes no 
Levels: no yes

> x <- factor(c(T,F,F,T))
> x
[1] TRUE  FALSE FALSE TRUE 
Levels: FALSE TRUE

> x <- factor(c(1+3i,1+4i,1+3i))
> x
[1] 1+3i 1+4i 1+3i
Levels: 1+3i 1+4i
```

使用table()统计各元素出现的次数：
```R
> x <- factor(c("yes","yes","no","yes","no"))
> table(x)
x
 no yes 
  2   3 
```

使用unclass()查看元素在R中的实际存储值（是一个整数）：
```R
> x <- factor(c("yes","yes","no","yes","no"))
> unclass(x)
[1] 2 2 1 2 1
attr(,"levels")
[1] "no"  "yes"
```

## factor中的顺序
factor中元素的顺序默认按照元素的自然序，如数字的大小、字符串的字典序，
亦可以显式指定元素顺序：
```R
> x <- factor(c("yes","yes","no","yes","no"),
+ levels=c("yes","no"))
> x
[1] yes yes no  yes no 
Levels: yes no
```



