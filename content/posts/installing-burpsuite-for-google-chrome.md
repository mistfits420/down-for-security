---
title: "How to install and configure Burpsuite for Google Chrome"
date: 2022-08-28T21:48:39+02:00
draft: false

cover:
    image: burp-1.png
Tags: ["Installation", "Configuration"]
Categories: ["Help"]
---

Installing Burpsuite is very simple

First step is to make sure your machine is up date.

`sudo apt-get update & upgrade`

After the installation is finished, it's time to install burpsuite. It can be installed easily by typing:

`sudo apt-get install burpsuite`

After opening burpsuite navigate to proxy > options:

![image](proxy2.png)

make sure you set the interface to `127.0.0.1:8080`

after you have set the interface, navigate back to proxy > intercept:

![image](intercept.png)

and make sure the interceptor is on like on the image above.



