# 数据容器

1、什么是数据容器

一种可以存储多个元素的python数据类型

2、Python有哪些数据容器

list(列表)、tuple（元组）、str（字符串）、set（集合）、dict（字典）

### 一、list列表

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-23-41-49-image.png)

1、列表的定义方法

[元素1，元素2，元素3，......]

2、什么是元素

数据容器内的的每一分数据，都称之为元素

3、元素的类型有限制吗？

元素的数据类型没有任何限制，甚至元素也可以是列表，这样就定义了嵌套列表

4、列表的特点

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-23-43-58-image.png)

#### （2）列表下标

1、列表的下标索引是什么？

列表的每一个元素，都有编号称之为下标索引

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-22-40-08-image.png)   

#### （3）列表的常用操作

1、查找某元素在列表内的下标索引

语法：列表.index(元素)

```python```
mylist = ["itcast", "itheima", "python"]

# 1.1 查找某元素在列表内的下标索引

index = mylist.index("itheima")
print(f"itheima在列表中的下标索引值是：{index}")

# 1.2如果被查找的元素不存在，会报错

# index = mylist.index("hello")

# print(f"hello在列表中的下标索引值是：{index}")

```
2、修改特定下标索引的值

```python```
mylist[0] = "传智教育"
print(f"列表被修改元素值后，结果是：{mylist}")
```

3、在指定下标位置插入新元素

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-22-49-35-image.png)

```python```
mylist.insert(1, "best")
print(f"列表插入元素后，结果是：{mylist}")

```
4、在列表的尾部追加```单个```新元素

```python```
mylist.append("黑马程序员")
print(f"列表在追加了元素后，结果是：{mylist}")
```

5、在列表的尾部追加```一批```新元素

```python```
mylist2 = [1, 2, 3]
mylist.extend(mylist2)

```
6、删除指定下标索引的元素（2种方式）

pop有返回值

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-22-52-05-image.png)

```python```
# 6.1 方式1：del 列表[下标]
del mylist[2]
print(f"列表删除元素后结果是：{mylist}")
# 6.2 方式2：列表.pop(下标)
mylist = ["itcast", "itheima", "python"]
element = mylist.pop(2)
print(f"通过pop方法取出元素后列表内容：{mylist}, 取出的元素是：{element}")
```

7、删除某元素在列表中的第一个匹配项

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-23-36-46-image.png)

```python```
mylist = ["itcast", "itheima", "itcast", "itheima", "python"]
mylist.remove("itheima")
print(f"通过remove方法移除元素后，列表的结果是：{mylist}")

```
8、清空列表

```python```
mylist.clear()
print(f"列表被清空了，结果是：{mylist}")
```

9、统计列表内某元素的数量

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-23-39-40-image.png)

```python```
mylist = ["itcast", "itheima", "itcast", "itheima", "python"]
count = mylist.count("itheima")
print(f"列表中itheima的数量是：{count}")

```
10、 统计列表中全部的元素数量

```python```
mylist = ["itcast", "itheima", "itcast", "itheima", "python"]
count = len(mylist)
print(f"列表的元素数量总共有：{count}个")
```

#### （4）列表循环遍历

![](E:\Learn\note\software_test_note\software_test_img\2022-10-15-23-51-40-image.png)

1、while循环

```python```
def list_while_func():
    """
    使用while循环遍历列表的演示函数
    :return: None
    """
    mylist = ["传智教育", "黑马程序员", "Python"]
    # 循环控制变量：通过下标索引来控制，默认是0
    # 每一次循环，将下标索引变量+1
    # 循环条件：下标索引变量 < 列表的元素数量

    # 定义一个变量，用来标记列表的下标
    index = 0       # 初始下标为0
    while index < len(mylist):
        # 通过index变量取出对应下标的元素
        element = mylist[index]
        print(f"列表的元素：{element}")
    
        # 至关重要：将循环变量（index）每一次循环都+1
        index += 1

```
2、for循环

```python```
def list_for_func():
    """
    使用for循环遍历列表的演示函数
    :return:
    """
    mylist = [1, 2, 3, 4, 5]
    # for 临时变量 in 数据容器:
    for element in mylist:
        print(f"列表的元素有：{element}")
```

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-07-55-image.png)
