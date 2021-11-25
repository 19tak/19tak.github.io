---
layout: post
title: "[Etc] Ubuntu, Python 버전 변경"
categories: [Etc, Tips]
tags: [Python, ubuntu]
fullview: false
comments: false
---

# 파이썬 실행 파일 확인

```console
$ ls /usr/bin/ | grep python
```

# Update-alternatives로 파이썬 버전 등록 및 변경

```console
$ sudo update-alternatives --config python
update-alternatives: error: no alternatives for python
```

<https://tttsss77.tistory.com/4>


---

## Alternatives

기본 커맨드의 심볼릭 링크를 관리해주는 리눅스 프로그램

데비안 계열 리눅스 (ubuntu)에서는 `update-alternatives`가 제공

---

# 참고

- **[JS 님의 포스팅](https://codechacha.com/ko/change-python-version/ "Ubuntu에서 Python 버전을 변경하는 방법")**
Ubuntu에서 Python 버전을 변경하는 방법

- **[Ubuntu Manpage: update-alternatives](http://manpages.ubuntu.com/manpages/trusty/man8/update-alternatives.8.html "Manpage")**
