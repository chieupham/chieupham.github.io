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

Install independencies:
```python
conda conda install tensorflow-gpu==1.8
```
