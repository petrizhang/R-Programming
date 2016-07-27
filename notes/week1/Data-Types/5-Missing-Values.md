# Data Types - Missing Values

## NA and NaN
- R中使用NA和NAN表示缺失值
- NaN表示非法的运算结果，其他缺失值则用NA表示

## is.na() and is.nan()
- is.na() 测试对象是否是NA
- is.nan() 测试对象是否是NaN
- NA有类型，例如integer NA，character NA
- NaN的类型则固定为numeric
- NaN一定是NA，反过来则不然

## 实例
```R
> x <- c(1, 2, NA, 10, 3)
> is.na(x)
[1] FALSE FALSE  TRUE FALSE FALSE
> is.nan(x)
[1] FALSE FALSE FALSE FALSE FALSE
```

```R
> x <- c(1, 2, NaN, NA, 4)
> is.na(x)
[1] FALSE FALSE  TRUE  TRUE FALSE
> is.nan(x)
[1] FALSE FALSE  TRUE FALSE FALSE
```

