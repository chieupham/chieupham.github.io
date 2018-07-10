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
passwd
```

Download and install miniconda:

```python
wget https://repo.continuum.io/miniconda/Miniconda2-latest-Linux-x86_64.sh
chmod +x Miniconda2-latest-Linux-x86_64.sh
./Miniconda2-latest-Linux-x86_64.sh
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
Copy a file or a folder to server via ssh
```python
rsync -avz -e 'ssh' /home/mymachine/dev/test.py name@ip:/home/name/
rsync -avz -e 'ssh' /home/mymachine/dev name@ip:/home/name/
```

Install some other platforms:
```python
pip install -r https://raw.githubusercontent.com/Lasagne/Lasagne/v0.1/requirements.txt
conda install theano=0.9 pygpu
conda install mkl-service
export MKL_THREADING_LAYER=GNU
```

Check my current path
```python
pwd
```

OK, that's all. Test some scripts.
