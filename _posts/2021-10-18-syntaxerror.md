---
layout: post
title: "[Etc] Python - 오류 / SyntaxError: Non-ASCII character '\xec' in file ~"
categories: [Etc, Errors]
tags: [python, error]
fullview: false
comments: false
---

# 오류 메세지

```
File "~.py", line 11
SyntaxError: Non-ASCII character '\xec\ in file ~.py on line 11, but no encoding declared; see http://python.org/dev/peps/pep-0263/ for details
```

---

# 원인

Python이 주석에 사용된 한글 문자의 인코딩을 이해할 수 없어서 발생한 것으로 판단 중.

---

# 해결 방법

## 1. 스크립트에 한글 지원 인코딩 선언해준다.

```
# -*- coding: utf-8 -*-
```

또는

```
# -*- coding: euc-kr -*-
```

두 가지 중에 하나를 스크립트의 맨 위에 선언 해주면 된다고 한다.

## 2. 한글 문자를 영어로 다 바꿔준다.

이건 필살기. ㅋ.ㅋ