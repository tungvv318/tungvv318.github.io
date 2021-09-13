---
layout: post
title: OOP in Python
date: 2021-09-13 19:10
summary: Hi, đây là bài viết giới thiệu về hướng đối tượng trong Python
categories: python
---

Chào các bạn, trong bài viết này mình sẽ giới thiệu những nội dung như sau:
* Class Attribute
* Static Method
* Class Method

### 1, Class Attribute
Class attribute là một thuộc tính thuộc về class, tức chúng ta có thể truy cập thông qua syntax <class_name>.<class_attribute>. Chúng ta cùng xem qua ví dụ sau nhé:

```python
class A:
  a = "Hello Tung"

x = A()
y = A()
print(x.a)
print(y.a)


# result
Hello Tung
Hello Tung
Hello Tung
```
Nếu chúng ta thay đổi thế này thì có chuyện gì xảy ra?

```python
x.a = "Hello Linh"
```
Câu lệnh trên đã tạo ra một instace attribute mới thay vì được tham chiếu tới class attribute.

```python
print(x.a)  # Hello Linh
print(y.a)  # Hello Tung
print(A.a)  # Hello Tung
```

Để chứng minh cho điều đó chúng ta hãy thực hiện câu lệnh:

```python
print(x.__dict__)
# {'a': 'Hello Linh'}
print(x.__class__.__dict__)
"""
{
    '__module__': '__main__',
    'a': "This is changing the class attribute 'a'!",
    '__dict__': <attribute '__dict__' of 'A' objects>,
    '__weakref__': <attribute '__weakref__' of 'A' objects>,
    '__doc__': None
}
"""
print(y.__dict__)
# {}
print(A.__dict__)
"""
{
    '__module__': '__main__',
    'a': "This is changing the class attribute 'a'!",
    '__dict__': <attribute '__dict__' of 'A' objects>,
    '__weakref__': <attribute '__weakref__' of 'A' objects>,
    '__doc__': None
}
"""
```

### 2, Static Method
### 3, Class Method