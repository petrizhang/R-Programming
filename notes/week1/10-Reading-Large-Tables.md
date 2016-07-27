# Reading Large Tables

## tips1-基础
- 细心读完read.table的帮助页
- 粗略计算待读取数据耗费的内存
- 设置commet.char = ""

## tips2-colClasses参数
使用read.table读取数据，若不指定colClasses参数，R会遍历全部数据来确定各列的合适类型，
显式地指定各列类型将大大缩短读取大型数据集的时间。

可以指定全部数据为同一类型：
```R
> t <- read.table("table.txt", colClasses = "character")
> t
  V1 V2 V3
1  1  2  a
2  3  4  b
3  5  6  c
> t[[1]]
[1] "1" "3" "5"
> class(t[[1]])
[1] "character"
```

可以读取前几行数据，使用sapply自动确定其类型，再读取全部数据：
```R
> initial <- read.table("table.txt",nrows=2)
> classes <- sapply(initial,class)
> classes
       V1        V2        V3 
"integer" "integer"  "factor" 
> tabAll <- read.table("table.txt", colClasses = classes)
> tabAll
  V1 V2 V3
1  1  2  a
2  3  4  b
3  5  6  c
```

## tips3-了解系统参数
- 系统内存多大？
- 本机正在运行任何其他应用？
- 本机存在其他用户？
- 操作系统？
- OS 32bit/64bit ?

## 计算数据集内存消耗
例 -
1,500,000行、120列的数据，类型为`numeric`，消耗的内存为：
```
1,500,000 × 120 × 8 bytes/numeric
= 1440000000 bytes
= 1440000000 / 2^20 bytes/MB
= 1373.29 MB
= 1.34 GB
```
