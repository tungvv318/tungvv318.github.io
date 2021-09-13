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

#### 1, Class Attribute
Class attribute là một thuộc tính thuộc về class, tức chúng ta có thể truy cập thông qua syntax <class_name>.<class_attribute>. Chúng ta cùng xem qua ví dụ sau nhé:

<iframe
  src="https://carbon.now.sh/embed?bg=rgba%28171%2C+184%2C+195%2C+1%29&t=one-dark&wt=none&l=python&ds=true&dsyoff=20px&dsblur=68px&wc=true&wa=true&pv=56px&ph=56px&ln=false&fl=1&fm=Hack&fs=14px&lh=133%25&si=false&es=2x&wm=false&code=class%2520A%253A%250A%2520%2520a%2520%253D%2520%2522Hello%2520Tung%2522%250A%250Ax%2520%253D%2520A%28%29%250Ay%2520%253D%2520A%28%29%250Aprint%28x.a%29%250Aprint%28y.a%29%250A%250A%2523%2520result%250AHello%2520Tung%250AHello%2520Tung"
  style="width: 302px; height: 389px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Nếu chúng ta thay đổi thế này thì có chuyện gì xảy ra?
```python
x.a = "Hello Linh"
```
