---
layout: post
title: "[Tips] Ubuntu, Python 버전 변경"
categories: [Etc, Tips]
tags: [Python, ubuntu]
fullview: false
comments: false
---

# 파이썬 실행 파일 확인

```console
$ ls /usr/bin/ | grep python
python
python2
python2.7
python3
python3.6
.....
```

다양한 버전의 파이썬 실행 파일을 확인 할 수 있다.

# Update-alternatives로 파이썬 버전 등록 및 변경

```console
$ sudo update-alternatives --config python
update-alternatives: error: no alternatives for python
```

초기에는 설정된 것이 없기 때문에 아무것도 뜨지 않는다.

```console
$ sudo update-alternatives --install /usr/bin/python python /usr/bin/python2.7 1
$ sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.6 2
```

원하는 버전의 파이썬을 다음과 같이 등록해주면

```console
$ sudo update-alternatives --config python
There are 2 choices for the alternative python (providing /usr/bin/python).

  Selection    Path                Priority   Status
------------------------------------------------------------
* 0            /usr/bin/python3.6   2         auto mode
  1            /usr/bin/python2.7   1         manual mode
  2            /usr/bin/python3.6   2         manual mode

Press <enter> to keep the current choice[*], or type selection number: 2
```

`sudo update-alternatives --config python` 명령어로 파이썬의 버전을 변경해 줄 수 있다.

---

## Alternatives

기본 커맨드의 심볼릭 링크를 관리해주는 리눅스 프로그램

데비안 계열 리눅스 (ubuntu)에서는 `update-alternatives`가 제공

---

# 참고

- **[JS 님의 포스팅](https://codechacha.com/ko/change-python-version/ "Ubuntu에서 Python 버전을 변경하는 방법")**
Ubuntu에서 Python 버전을 변경하는 방법

- **[Ubuntu Manpage: update-alternatives](http://manpages.ubuntu.com/manpages/trusty/man8/update-alternatives.8.html "Manpage")**
