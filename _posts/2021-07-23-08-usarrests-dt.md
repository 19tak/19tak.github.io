---
layout: post
title: "[08] R, USArrests 데이터 분석 - Decision Tree "
categories: [R, KFQ]
tags: [R, KFQ, USArrests, decision tree, assignment]
fullview: false
comments: false
---

#### dplyr


![image](https://user-images.githubusercontent.com/84369912/126749359-377dd488-1d89-472d-ba25-99194e7f6c56.png)

![image](https://user-images.githubusercontent.com/84369912/126749380-6911d01b-4c0d-4a1d-a434-78104b823593.png)

![image](https://user-images.githubusercontent.com/84369912/126749393-15b566b4-58cf-4686-9eee-38ffe0a75e0e.png)

## 결과 해석
```
n= 50 

node), split, n, deviance, yval
      * denotes terminal node

 1) root 50 10266.4200 65.54000  
   2) Rape< 17.55 21  4368.9520 58.04762  
     4) Assault< 94 9  1100.0000 50.66667 *
     5) Assault>=94 12  2410.9170 63.58333 *
   3) Rape>=17.55 29  3864.9660 70.96552  
     6) Murder>=12.45 7   847.7143 64.42857 *
     7) Murder< 12.45 22  2622.9550 73.04545  
      14) Rape< 21.2 7  1018.8570 69.14286 *
      15) Rape>=21.2 15  1447.7330 74.86667 *
```

50개의 주에서 10만명 당

- 강간 체포 수가 17.55 미만이고, 폭행 체포 수가 94 미만인 주 9개, 도시 인구 50.7%
- 강간 체포 수가 17.55 미만이고, 폭행 체포 수가 94 이상인 주 12개, 도시 인구 63.58%
- 강간 체포 수가 17.55 이상이고, 살인 체포 수가 12.45 이상인 주 7개, 도시 인구 64.4%
- 강간 체포 수가 17.55 이상 21.2 미만, 살인 체포 수가 12.45 미만인 주 7개, 도시 인구 69.1%
- 강간 체포 수가 21.2 이상이고, 살인 체포 수가 12.45 미만인 주 15개, 도시 인구 74.9%
+ 살인에 비해 강간비율이 높은 주가 인구가 많다.