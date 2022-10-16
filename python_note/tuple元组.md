### tuple元组

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-10-21-image.png)

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-27-51-image.png)

1、定义元组

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-10-43-image.png)

```python```
t1 = (1, "Hello", True)
t2 = ()
t3 = tuple()
print(f"t1的类型是：{type(t1)}, 内容是：{t1}")
print(f"t2的类型是：{type(t2)}, 内容是：{t2}")
print(f"t3的类型是：{type(t3)}, 内容是：{t3}")
```

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-12-52-image.png)

2、定义单个元素的元素

注意：元组只有一个数据，这个数据后面要添加逗号。

如果不添加逗号，那么定义的不是元组（tuple）类型而是字符串（str）类型

```python```
t4 = ("hello", )
print(f"t4的类型是：{type(t4)}, t4的内容是：{t4}")
```

 3、元组的嵌套

```python```
t5 = ( (1, 2, 3), (4, 5, 6) )
print(f"t5的类型是：{type(t5)}, 内容是：{t5}")
```

取出元素

```python```
num = t5[1][2]
print(f"从嵌套元组中取出的数据是：{num}")
```

4、元组的操作

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-20-00-image.png)

```python```
# 元组的操作：index查找方法
t6 = ("传智教育", "黑马程序员", "Python")
index = t6.index("黑马程序员")
print(f"在元组t6中查找黑马程序员，的下标是：{index}")
# 元组的操作：count统计方法
t7 = ("传智教育", "黑马程序员", "黑马程序员", "黑马程序员", "Python")
num = t7.count("黑马程序员")
print(f"在元组t7中统计黑马程序员的数量有：{num}个")
# 元组的操作：len函数统计元组元素数量
t8 = ("传智教育", "黑马程序员", "黑马程序员", "黑马程序员", "Python")
num = len(t8)
print(f"t8元组中的元素有：{num}个")
```

5、元组的遍历

（1）while循环

```python```
# 元组的遍历：while
index = 0
while index < len(t8):
    print(f"元组的元素有：{t8[index]}")
    # 至关重要
    index += 1
```

（2）for循环

```python```
# 元组的遍历：for
for element in t8:
    print(f"2元组的元素有：{element}")
```

6、元组不可修改

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-25-30-image.png)

7、元组特点

![](E:\Learn\note\software_test_note\software_test_img\2022-10-16-00-27-11-image.png)
































