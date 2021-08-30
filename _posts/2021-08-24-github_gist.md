---
layout: post
title: "[Etc] 깃허브 블로그에 이쁜 코드 블럭, Github Gist 사용 "
categories: [Etc, Tips]
tags: [github blog, github, blog, jekyll, code block, github gist, gist]
fullview: false
comments: false
---

# Github Gist

코드를 작성하고, **HTML Embed 태그**를 이용해서 코드 블럭을 이쁘게~ 나타낼 수 있다.

URL: <https://gist.github.com/>

---

## 비교

<script src="https://gist.github.com/19tak/16058e667e7eff94cfc6f58a4f5e22ea.js"></script>

```
// default zoom
var zoom = 17;
// center of the map
var center = [37.558240, 127.000258];
// Create the map
var map = L.map('map', { attributionControl: false }).setView(center, zoom);

// Set up the OSM layer
L.tileLayer('http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', { maxZoom: 18 }).addTo(map);

// add a marker in the given location
L.marker(center)
.bindPopup("내가 졸업한 동국대학교")
.on("mouseover",function(evt){this.openPopup();})
.on("mouseout",function(evt){this.closePopup();}).addTo(map);
```

---

# 참고

- **[eona1301 님의 포스팅](https://velog.io/@eona1301/Github-Blog-MarkDown-%EC%BD%94%EB%93%9C-%EC%9E%91%EC%84%B1 "[Github Blog] MarkDown 코드 작성")**
[Github Blog] MarkDown 코드 작성