# Reading Tabular Data

## 读数据
- read.table, read.csv读取表结构数据
- readLines读取文本文件指定行数
- source读取R代码文件
- dget读取R代码文件
- load读取保存过的工作空间
- unserialize读取被序列化为二进制的R对象

## 写数据
与读数据对应
- write.table
- writeLines
- dump
- dput
- save
- serialize

## read.table
最常用的读取数据的函数，重要参数有：

|参数|类型|含义|  
|---|---|---|  
| file | character|文件名|  
| header | logical| 数据是否有一行表头|  
| sep |charater|列划分的方式|  
| colClassese|character vector|每一列的类型|  
| nrows|integer|行数|  
| comment.char| character| 注释字符串|  
| skip| integer| 跳过多少行开始读数据|  
|stringAsFactors| logical| 字符串是否解释成factor|  

下面是table.txt中的内容
```
1 2 a
3 4 b
5 6 c
# this is a table
```
直接读入：
```R
> t <- read.table("rstudio/table.txt")
> t
  V1 V2 V3
1  1  2  a
2  3  4  b
3  5  6  c
```
默认情况下注释符号为`#`，且R会自动确定各列的类型。

## read.csv
与read.table区别在于列的分隔符是`,`
