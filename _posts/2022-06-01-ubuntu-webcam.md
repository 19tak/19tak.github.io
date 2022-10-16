---
layout: post
title: "[Tips] ubuntu 카메라 디바이스 관련, v4l2"
categories: [Etc, Errors]
tags: [ubuntu, webcam]
fullview: false
comments: false
---

# 카메라 디바이스

우분투 환경에서 카메라 등의 디바이스가 설치 되어있을 때 확인하는 방법이 여러가지가 있다.

프로젝트를 진행하며 Usb 웹 캠을 사용했고, 디바이스 번호 및 호환 해상도 등을 확인하기 위해 사용했다.

```console
dmesg | grep -i "Camera"
ls -ltrh /dev/video*
v4l2-ctl --list-devices
```

## v4l2

**v4l2**가 있다면 다음의 메세지로 편하게 확인할 수 있다.

```console
sudo apt install v4l-utils
v4l2-ctl --list-devices
v4l2-ctl --list-formats-ext
```

`--list-devices` 옵션으로는 모든 카메라 디바이스를 확인할 수 있다.

`--listformats-ext` 옵션은 디바이스의 지원 해상도를 확인 할 수 있다.

특정 디바이스의 정보만을 확인하기 위해서는 `-d` 옵션으로 디바이스를 지정해준다.

```console
v4l2-ctl -d /dev/video0 --list-formats
```

---

외에도 치즈와 guvc 등 다른 카메라 연동 프로그램들이 있다고는 하는데

개인적으로는 **v4l2**에 익숙해지는 것이 가장 편한 것 같다.

```console
sudo apt install cheese
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