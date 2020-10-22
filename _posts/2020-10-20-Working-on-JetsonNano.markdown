---
layout: post
comments: true
title:  "Working on Jetson Nano"
excerpt: "(Working on Jetson Nano)"
date:   2020-10-20 13:00:00
mathjax: false
---
1) wired device not managed (https://askubuntu.com/questions/71159/network-manager-says-device-not-managed)

```python
sudo nano /etc/NetworkManager/NetworkManager.conf
```

change the line managed=false to managed=true
Save, stop and start network manager:

```python
sudo service network-manager restart
```

2) Install pygame sdl-config not found (https://stackoverflow.com/questions/19579528/pygame-installation-sdl-config-command-not-found)

```python
python3 -m pip install pygame
```

3) Install pytorch from wheel !

4) Install spyder : https://programmer.help/blogs/jetson-agx-xavier-installs-spyder3-in-ubuntu-18.04.html

