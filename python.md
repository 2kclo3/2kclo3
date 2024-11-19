# Python 学习

---

**基础语法** **1. 注释**  
- 单行注释：使用 `#`
 
- 多行注释：使用三个单引号 `'''` 或三个双引号 `"""`


```python
# 这是单行注释
'''
这是
多行注释
'''
```


---

**2. 变量与数据类型**  
- **变量** ：动态类型，不需要声明类型，直接赋值。
 
- **常见数据类型** ： 
  - `int`：整数
 
  - `float`：浮点数
 
  - `str`：字符串
 
  - `bool`：布尔值 (`True`/`False`)
 
  - `None`：空值
 
  - `list`：列表
 
  - `tuple`：元组
 
  - `dict`：字典
 
  - `set`：集合


```python
# 示例
a = 10                # int
b = 3.14              # float
c = "Hello, Python!"  # str
d = True              # bool
e = None              # None
```


---

**3. 运算符**  
- **算术运算符** ：`+`, `-`, `*`, `/`, `//` (整除), `%` (取模), `**` (幂运算)
 
- **比较运算符** ：`==`, `!=`, `>`, `<`, `>=`, `<=`
 
- **逻辑运算符** ：`and`, `or`, `not`
 
- **赋值运算符** ：`=`, `+=`, `-=`, `*=`, `/=`
 
- **成员运算符** ：`in`, `not in`


```python
# 示例
x, y = 5, 3
print(x + y)   # 8
print(x // y)  # 1
print(x > y)   # True
print(x == y)  # False
```


---

**4. 条件语句** 

```python
# 示例
x = 10
if x > 0:
    print("正数")
elif x < 0:
    print("负数")
else:
    print("零")
```


---

**5. 循环语句**  
- **for 循环** ：用于遍历序列（如列表、字符串）。
 
- **while 循环** ：满足条件时循环。


```python
# for 循环
for i in range(5):
    print(i)

# while 循环
x = 5
while x > 0:
    print(x)
    x -= 1
```
 
- **循环控制** ： 
  - `break`：跳出循环
 
  - `continue`：跳过本次循环


---

**数据结构** **1. 列表 (list)** 

```python
# 列表操作
lst = [1, 2, 3, 4]
lst.append(5)      # 添加元素
lst.remove(2)      # 移除元素
print(lst[1])      # 访问元素
print(len(lst))    # 列表长度
```


---

**2. 字典 (dict)** 

```python
# 字典操作
d = {"name": "Alice", "age": 25}
d["city"] = "New York"   # 添加键值对
print(d["name"])         # 访问键值对
print(d.keys())          # 获取所有键
print(d.values())        # 获取所有值
```


---

**3. 元组 (tuple)** 

```python
# 元组操作
t = (1, 2, 3)
print(t[0])     # 访问元素
```


---

**4. 集合 (set)** 

```python
# 集合操作
s = {1, 2, 3}
s.add(4)        # 添加元素
s.remove(2)     # 移除元素
```


---

**字符串操作** 

```python
s = "Hello, World!"

# 常见方法
print(s.lower())         # 全部小写
print(s.upper())         # 全部大写
print(s.strip())         # 去除首尾空格
print(s.split(","))      # 按指定字符分割
print(s.replace("World", "Python"))  # 替换字符串
```


---

**函数** 

```python
# 函数定义
def add(a, b):
    return a + b

# 调用函数
result = add(3, 5)
print(result)
```


---

**文件操作** 

```python
# 文件读取
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

# 文件写入
with open("example.txt", "w") as file:
    file.write("Hello, File!")
```


---

**异常处理** 

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("除数不能为零！")
finally:
    print("程序结束")
```


---

**面向对象编程 (OOP)** 

```python
# 定义类
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"{self.name} 叫了一声")

# 创建对象
dog = Animal("狗")
dog.speak()
```


---

**常用标准库** **1. math** 

```python
import math
print(math.sqrt(16))  # 开平方
```
**2. random** 

```python
import random
print(random.randint(1, 10))  # 随机整数
```
**3. datetime** 

```python
from datetime import datetime
print(datetime.now())  # 当前时间
```
**4. os** 

```python
import os
print(os.getcwd())  # 获取当前工作目录
```


---

**进阶内容** **1. 列表推导式** 

```python
squares = [x**2 for x in range(10)]
print(squares)
```
**2. lambda 表达式** 

```python
# 匿名函数
add = lambda x, y: x + y
print(add(2, 3))
```
**3. 装饰器** 

```python
def decorator(func):
    def wrapper():
        print("装饰器功能")
        func()
    return wrapper

@decorator
def say_hello():
    print("Hello")

say_hello()
```
**4. 生成器** 

```python
def generate_numbers():
    for i in range(5):
        yield i

for num in generate_numbers():
    print(num)
```
**5. 文件操作** 

```python
import json

# JSON 序列化
data = {"name": "Alice", "age": 25}
with open("data.json", "w") as file:
    json.dump(data, file)

# JSON 反序列化
with open("data.json", "r") as file:
    data = json.load(file)
    print(data)
```

