---
layout: post
title: "[Etc] ubuntu, terminator ctrl + shift + e 가 안될 때 "
categories: [Etc, Tips]
tags: [ubuntu, terminator, ubuntu terminator, ibus]
fullview: false
comments: false
---

# Terminator

ros 구동은 기본적으로 터미널 창에서 이루어진다. 따라서 여러개의 터미널 창의 사용은 필수적.

이에 나는 다중 터미널 창을 추천한다. 내가 사용하는 것은 **terminator**

```
sudo apt-get install terminator
```

---

# Terminator 주요 단축키

| 단축키 설명 | 사용법 |
| --- | :---: |
| 터미네이터 <br> 실행 | ctrl + alt + t |
| 터미네이터 <br> 종료 | ctrl + shift + q |
| 수평 분할 | ctrl + shift + o |
| 수직 분할 | ctrl + shift + e |
| 분할 창 이동 | ctrl + shift + p |
| 분할 창 이동 <br> (반대 방향) | ctrl + shift + m |
| 분할 창 종료 | ctrl + shift + w |
| 분할 창 확대 | ctrl + shift + x |

---

# 문제점

<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>E</kbd> 가 작동을 안 할 때가 있다.

---

# 원인

키보드 세팅에 이미 <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>E</kbd> 가 있어서 생긴다.

나의 경우엔 키보드 입력기가 **ibus**일 때, 이모지 단축키로 되어있었다.

---

# 해결 방법

## **ibus** 세팅에 들어간다.

```
ibus-setup
```

에모지 주석을 삭제, 또는 변경 해주자.

![스크린샷, 2021-08-27 21-56-45](https://user-images.githubusercontent.com/84369912/131159812-2cede012-a180-41ab-9b84-4b4a6a781943.png)

![스크린샷, 2021-08-27 21-56-50](https://user-images.githubusercontent.com/84369912/131159886-78e3c4bd-dfec-4353-949f-84f4c3183c55.png)

---

# 참고

- **[snowdeer 님의 포스팅](https://snowdeer.github.io/mac-os/2020/09/22/ctrl-shift-e-key-on-ubuntu-20p04/ "Ctrl + Shift + E 명령어가 안 먹히는 경우(Terminator)")**
Ctrl + Shift + E 명령어가 안 먹히는 경우(Terminator)