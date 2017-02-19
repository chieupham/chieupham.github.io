---
layout: post
comments: true
title:  "Bài: Cài đặt Python và thư viện sử dụng Anaconda trên Windows"
excerpt: "Phụ blog Machine Learning cơ bản."
date:   2017-02-18 13:00:00
mathjax: false
---

Trong bài này, tôi sẽ giúp các bạn làm quen với Python trên Windows theo cách đơn giản nhất. 

## 1. Cài đặt Python bằng Anaconda.
Để tải về Python và một số thư viện cần thiết, một cách đơn giản nhất là tải về [Anaconda cho windows](https://docs.continuum.io/anaconda/install#anaconda-for-windows-install/) và cài đặt vào thư mục bạn muốn. Anaconda hỗ trợ rất nhiều thư viện giúp lập trình Python. 

Sau khi cài đặt xong, bạn vào thư mục Scripts trong thư mục Anaconda vừa cài đặt, và khởi động Spyder. Các bạn có thể sử dụng môi trường IDE nào cũng được. Tôi hay sử dụng Spyder vì layout của nó khá giống với Matlab, chúng ta có thể quan sát được Script, Console và các biến. Console cho Python của Spyder bao gồm Python hoặc IPython notebook. Cá nhân tôi thích Python Console hơn.

<div class="imgcap">
<img src ="/assets/PythonWindows/spyder.PNG" width = "700" align = "center">
<div class="thecap"> Giao diện Spyder trên Windows. <br></div>
</div>

## 2. Kiểm tra Libs
Anaconda đã có sẵn khá là nhiều thư viện python như : [Numpy](http://www.numpy.org/), [Scipy](https://www.scipy.org/), [Matplotlib](http://matplotlib.org/) , [sklearn](http://scikit-learn.org/stable/)

Để kiểm tra python của Anaconda đã có thư viện nào đó, chúng ta sẽ thử import nó trong Console.

```python
>>> import numpy
```
Không có lỗi được thông báo nghĩa là python đã biết được thư viện này. Để kiểm tra thư viện này ở đâu, ta truy xuất *__file__* của thư viện như sau:
```python
>>> numpy.__file__
'C:\\These\\soft\\Anaconda2\\lib\\site-packages\\numpy\\__init__.pyc'
```
Thư viện Numpy của tôi nằm ở đường dẫn *'C:\\These\\soft\\Anaconda2\\lib\\site-packages\\'* . Anaconda đã có sẵn thư viện Numpy

```python
>>> import sklearn
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ImportError: No module named sklearn
```
Nếu như Python trả về lỗi Import như trên thì có nghĩa trong Anaconda chúng ta chưa có thư viện đó.

##  3. Cài đặt Libs bằng Anaconda
Ở phần trên python của tôi chưa có thư viện *sklearn*, nên tôi phải đi cài đặt nó. Vì tôi sử dụng Anaconda cho lập trình python nên tôi cần phải *cài đặt thư viện mới vào đường dẫn libs python của Anaconda* hoặc *chỉ cho python biết về đường dẫn tới thư viện mới này*.

Với Anaconda, việc cài đặt 1 thư viện đang được hỗ trợ cực kỳ đơn giản, tôi chỉ cần dùng tools *pip* hoặc *conda* mà Anaconda đã cài sẵn. Cụ thể, ở đây tôi muốn cài thư viện sklearn tôi truy cập vào trang chủ của [sklearn] (http://scikit-learn.org/stable/install.html). Trang này ghi rằng chúng ta có thể cài bằng *pip* hoặc *conda*.

Chúng ta sẽ bật cmd (Command Prompt) của windows lên và gõ lệnh *conda install scikit-learn* hoặc *pip install -U scikit-learn*. Conda sẽ tự động tìm thư viện *sklearn* và cài vào đường dẫn Anaconda giúp chúng ta.

```python
C:>conda install scikit-learn
```
<div class="imgcap">
<img src ="/assets/PythonWindows/cmd_conda.png" width = "600" align = "center">
<div class="thecap"> Sử dụng conda qua cmd của windows. <br></div>
</div>

Chờ cho thư viện và các thư viện liên quan hoàn tất cài đặt, chúng ta vào spyder kiểm tra lại đã có *sklearn* chưa. Và python trả về đã có sklearn trong Anaconda. Và chúng ta đã có thể sử dụng sklearn.
```python
>>> import sklearn
>>> sklearn.__file__
'C:\\These\\soft\\Anaconda2\\lib\\site-packages\\sklearn\\__init__.pyc'
>>> 
```

## 4. Chạy thử 1 đoạn code trên python.

Bây giờ, các bạn đã có thể chạy thử 1 vài ví dụ trên trang Machine Learning cơ bản, ví dụ như [Bài 3: Linear Regression](https://tiepvupsu.github.io/2016/12/28/linearregression/)


