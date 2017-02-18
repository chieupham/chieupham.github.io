---
layout: post
comments: true
title:  "Bài: Làm quen với Python và một số thư viện (sử dụng Anaconda)"
excerpt: "Phụ blog Machine Learning cơ bản."
date:   2017-02-18 13:00:00
mathjax: false
---

Trong bài này, tôi sẽ giúp các bạn làm quen với Python trên Windows theo cách đơn giản nhất. 
Tôi chỉ sử dụng Ubuntu cho việc lập trình nên bài này sẽ có rất nhiều hạn chế.

## 1. Cài đặt Python bằng Anaconda.
Để tải về Python và một số thư viện cần thiết, một cách đơn giản nhất là tải về [Anaconda cho windows](https://docs.continuum.io/anaconda/install#anaconda-for-windows-install/) và cài đặt vào thư mục bạn muốn. Anaconda hỗ trợ rất nhiều thư viện giúp lập trình Python. 

Sau khi cài đặt xong, bạn vào thư mục Scripts trong thư mục Anaconda vừa cài đặt, và khởi động Spyder. Các bạn có thể sử dụng môi trường IDE nào cũng được. Tôi hay sử dụng Spyder vì layout của nó khá giống với Matlab, chúng ta có thể quan sát được Script, Console và các biến. Console cho Python của Spyder bao gồm Python hoặc IPython notebook. Cá nhân tôi thích Python Console hơn.

<div class="imgcap">
<img src ="/assets/PythonWindows/spyder.PNG" width = "500" align = "center">
<div class="thecap"> Giao diện Spyder trên Windows. <br></div>
</div>

## 2. Cài đặt Libs
Anaconda đã có sẵn khá là nhiều thư viện python như : [Numpy](http://www.numpy.org/), [Scipy](https://www.scipy.org/), [Matplotlib](http://matplotlib.org/) , [sklearn](http://scikit-learn.org/stable/)

Để kiểm tra python của Anaconda đã có thư viện nào đó, chúng ta sẽ thử import nó trong Console.

```python
import numpy
```
Không có lỗi gì được thông báo nghĩa là python đã biết được thư viện.

```python
>>> import nilearn
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ImportError: No module named nilearn
```
Nếu như Python trả về lỗi Import như trên thì có nghĩa trong Anaconda chúng ta chưa có thư viện đó.

# 
