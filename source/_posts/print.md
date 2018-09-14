---
title: print的打印和输出
tags:
  - python
---

> 在 Python 中， `print`可以打印所有变量数据，
包括自定义类型。

> 在 2.x 版本中， `print`是个语句，但在 3.x 中却
是个内置函数，并且拥有更丰富的功能。
<!-- more -->
# **参数选项**

可以用 `help(print)`来查看 `print`函数的参数解释。
```
print(...) 
    print(value, ..., sep=' ', end='\n',fi
le=sys.stdout, flush=False)
 
    Prints the values to a stream, or to s
ys.stdout by default. 
    Optional keyword arguments: 
    file: a file-like object (stream); def
aults to the current sys.stdout. 
    sep: string inserted between values, d
efault a space. 
    end: string appended after the last va
lue, default a newline. 
    flush: whether to forcibly flush the s
tream.
```
**value**: 打印的值，可多个

**file**: 输出流，默认是`sys.stdout`

**sep**: 多个值之间的分隔符

**end**: 结束符，默认是换行符 `\n`

**flush**: 是否强制刷新到输出流，默认否

# **能打印任意数据**

打印数字、字符串、布尔值
```
print(1024, 10.24, 'hello', False) 
# 1024 10.24 hello False
```
打印列表
```
print([1, 2, 3]) 
# [1, 2, 3]
```
打印元组
```
print((1, 2, 3)) 
# (1, 2, 3)
```
打印字典
```
print({'name': 'hello', 'age': 18}) 
# {'name': 'hello', 'age': 18}
```
打印集合
```
print({1, 2, 3}) 
# {1, 2, 3}
```
打印对象
```
class Demo: 
    pass

 
demo = Demo() 
print(demo)

# <__main__.Demo object at 0x1005bae80>
```
# **分隔符**

默认分隔符是空格， sep 参数可以修改。
```
print(1, 2, 3, sep='-') 
# 1-2-3
```
# **结束符**

默认结束符是行号， end 参数可以修改。
```
print('第一行', end='-')
print('第二行') 
# 第一行-第二行
```
# **输出重定向**

默认情况下， `print`函数会将内容打印输出到标准输
出流(即 `sys.stdout)`，可以通过 file 参数自定
义输出流。
```
with open('data.log', 'w') as fileObj: 
    print('hello world!', file=fileObj)
```
> 此时，不会有任何标准输出，但对应的文件中已经有了
内容。

> 我们也可以输出到错误输出流，例如：

```
import sys
 
print('hello world!', file=sys.stderr)
```