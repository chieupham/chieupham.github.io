---
layout: post
comments: true
title:  "Working with Jetson Nano"
excerpt: "(Working with Jetson Nano)"
date:   2020-10-20 13:00:00
mathjax: false
---
1): wired device not managed (https://askubuntu.com/questions/71159/network-manager-says-device-not-managed)

```python
sudo nano /etc/NetworkManager/NetworkManager.conf
```

change the line managed=false to managed=true
Save, stop and start network manager:

```python
sudo service network-manager restart
```
