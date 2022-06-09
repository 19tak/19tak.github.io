---
layout: post
title: "ubuntu webacm"
categories: [Study, Algorithm]
tags: [Python, Algorithm]
fullview: false
comments: false
---

```console
dmesg | grep -i "Camera"
ls -ltrh /dev/video*
v4l2-ctl --list-devices
```

```console
sudo apt install cheese
```

---

```console
sudo apt install v4l-utils
v4l2-ctl --list-devices
v4l2-ctl --list-formats-ext
```

```console
sudo apt install guvcview
```
---

# 참고

- **[Lubos Rendek 님의 포스팅](https://linuxconfig.org/how-to-test-webcam-on-ubuntu-20-04-focal-fossa "How to test webcam on Ubuntu 20.04 Focal Fossa")**
How to test webcam on Ubuntu 20.04 Focal Fossa

- **[Dave Jansen 님의 포스팅](https://davejansen.com/logitech-streamcam-on-linux/ "Using a Logitech StreamCam on Linux")**
Using a Logitech StreamCam on Linux

- **[미니멀공대생 님의 포스팅](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=nswve&logNo=221483691234 "ROS:: usb캠 사용하기, fps 향상 (usb_cam, logitech c920)")**
ROS:: usb캠 사용하기, fps 향상 (usb_cam, logitech c920)

- **[Wonjae Cho 님의 포스팅](http://chofukutomi.blogspot.com/2017/01/usb-camera-ros-kinetic-ubuntu-1604.html "[참고] ROS kinetic에서 WebCam 사용하기 (Ubuntu 16.04)")**
[참고] ROS kinetic에서 WebCam 사용하기 (Ubuntu 16.04)