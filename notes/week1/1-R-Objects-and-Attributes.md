#Data Types - R Objects and Attributes

## 基本类型
- 字符  
- 小数  
- 整数
- 复数
- logical(True/False)

## vector
- vector的元素必须为同种类型
- list的则可以包含不同类的元素
- vector()创建空向量

## 数字
- 所有数字常量为浮点数
- 使用后缀L显式指定整型，如"10L"
- 内置`Inf`表示无穷
- 内置`NaN`表示非数字或缺失值

## 属性
R对象的常见属性有
- names, dimnames
- dimensions(e.g. matrix, arrays)
- class
- length
- 用户定义的属性/metadata

attributes()函数可以查看或修改R对象的属性


