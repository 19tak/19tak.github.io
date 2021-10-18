---
layout: post
title: "[Etc] ubuntu 20.04 / 18.04, Github Desktop 설치 "
categories: [Etc, Tips]
tags: [ubuntu, github desktop]
fullview: false
comments: false
---

## 1. Github Desktop.deb 다운로드

```
sudo wget https://github.com/shiftkey/desktop/releases/download/release-2.9.0-linux2/GitHubDesktop-linux-2.9.0-linux2.deb
```

## 2. gdebi-core 설치

```
sudo apt-get install gdebi-core
```

## 3. gdebi로 Github Desktop 설치

```
sudo gdebi GitHubDesktop-linux-2.9.0-linux2.deb
```

---

# gdebi

데비안 계열의 패키지 설치 파일인 .deb 파일을 GUI로 손쉽게 설치할 수 있도록 해주는 패키지

저장소 외 인터넷에서 내려받은 .deb 파일을 이용해 패키지를 설치하는 프로그램

deb 파일에 저장된 정보를 통해 패키지 의존성을 확인하고 설치할 수 있다

## 예제

```
gdebi foo_1.0_all.deb
gdebi foo-1.0/debian/control
```

---

# 참고

- **[기계지니 님의 포스팅](https://haaringa.tistory.com/entry/깃허브-데스크탑-Github-desktop-리눅스에서-사용하기 "깃허브-데스크탑-Github-desktop-리눅스에서-사용하기")**
깃허브-데스크탑-Github-desktop-리눅스에서-사용하기

- **[Danyson 님의 포스팅](https://dev.to/danyson/how-to-install-github-desktop-for-ubuntu-debian-4hko "How to install Github Desktop for Ubuntu & Debian?")**
How to install Github Desktop for Ubuntu & Debian?

- **[Ubuntu Manpage: gdebi - Simple tool to install deb files](http://manpages.ubuntu.com/manpages/bionic/man1/gdebi.1.html "Manpage")**

- **[gdebi in Launchpad](https://launchpad.net/gdebi/ "Launchpad")**