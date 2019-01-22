---
layout: post
comments: true
title:  "Installing Tensorflow"
excerpt: "(Working at Paristech)"
date:   2019-01-21 13:00:00
mathjax: false
---

Python 3, GPU GTX

Download and install miniconda:

```python
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod +x Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
export PATH="/home/chpham/miniconda3/bin:$PATH"
```

Install tensorflow:
```python
conda install tensorflow-gpu==1.8
```

22/01/2019, Installing Theano in order to test http://bethgelab.org/media/uploads/dynamic_textures/ (FAIL: Old versions of Theano and Lasagne)
```python
pip install theano==0.7
pip install Lasagne==0.1
pip install scikit-image
pip install scikit-learn
```
