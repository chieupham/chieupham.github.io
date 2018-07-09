---
layout: post
comments: true
title:  "Installing Keras for one user in server (Linux)"
excerpt: "(Working with server)"
date:   2018-07-09 13:00:00
mathjax: false
---

Python 2.7, GPU Titan Xp

Access a machine in server and changing password:

```python
ssh name@ip
pwd
```

Download and install miniconda:

```python
wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
chmod +x Miniconda2-latest-Linux-x86_64.sh
```

Install independencies:
```python
conda install -c anaconda cudatoolkit
conda install -c anaconda cudnn 
```

Install Tensorflow and Keras
```python
pip install --upgrade tensorflow-gpu
pip install keras
```

Install SimpleITK for loading NIFTI
```python
pip install SimpleITK
```

OK, that's all. Test some scripts.
