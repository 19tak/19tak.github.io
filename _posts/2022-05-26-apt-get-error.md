---
layout: post
title: "apt-get error"
categories: [Study, Algorithm]
tags: [Python, Algorithm]
fullview: false
comments: false
---

```shell
root@Desktop:/mnt/c/Users$ sudo apt --fix-missing update
Hit:1 http://security.ubuntu.com/ubuntu bionic-security InRelease
Hit:2 http://kr.archive.ubuntu.com/ubuntu bionic InRelease
Hit:4 http://kr.archive.ubuntu.com/ubuntu bionic-backports InRelease
Get:3 http://kr.archive.ubuntu.com/ubuntu bionic-updates InRelease [88.7 kB]
Get:5 http://kr.archive.ubuntu.com/ubuntu bionic-updates/main amd64 Packages [1034 kB]
Get:6 http://kr.archive.ubuntu.com/ubuntu bionic-updates/main Translation-en [347 kB]
Get:7 http://kr.archive.ubuntu.com/ubuntu bionic-updates/restricted amd64 Packages [84.7 kB]
Get:8 http://kr.archive.ubuntu.com/ubuntu bionic-updates/restricted Translation-en [18.7 kB]
Get:9 http://kr.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 Packages [1097 kB]
Err:9 http://kr.archive.ubuntu.com/ubuntu bionic-updates/universe amd64 Packages
  Hash Sum mismatch
  Hashes of expected file:
   - Filesize:1097184 [weak]
   - SHA256:46824ffcb2d3fcdjfhbje3eb417e3f25b49e8929644621c1d64djnwiorewfe31bc
   - SHA1:dc07575d9d383bfdefgnji239819755e5ef44f [weak]
   - MD5Sum:3f0a5f1e283914818aaa044ceb3d [weak]
  Hashes of received file:
   - SHA256:614d04fa59f6f2541e8ddcc320baa8eajfsklf978dc3283911f0cca3516a98e7
   - SHA1:23bhkgcca9d2f334dsjfnjke7285ecdfd11b1c74 [weak]
   - MD5Sum:23nj4k3fjkower3a97509ac5c1720cc2 [weak]
   - Filesize:1097184 [weak]
  Last modification reported: Sun, 16 Aug 2020 00:53:49 +0000
  Release file created at: Mon, 17 Aug 2020 06:50:31 +0000
Get:10 http://kr.archive.ubuntu.com/ubuntu bionic-updates/universe Translation-en [342 kB]
Get:11 http://kr.archive.ubuntu.com/ubuntu bionic-updates/multiverse amd64 Packages [19.2 kB]
Get:12 http://kr.archive.ubuntu.com/ubuntu bionic-updates/multiverse Translation-en [6712 B]
Fetched 1186 kB in 4s (337 kB/s)
Reading package lists... Done
E: Failed to fetch http://kr.archive.ubuntu.com/ubuntu/dists/bionic-updates/universe/binary-amd64/by-hash/SHA256/46824ffcb2d3fcdjfhbje3eb417e3f25b49e8929644621c1d64djnwiorewfe31bc  Hash Sum mismatch
   Hashes of expected file:
    - Filesize:1097184 [weak]
    - SHA256:46824ffcb2d3fcdjfhbje3eb417e3f25b49e8929644621c1d64djnwiorewfe31bc
    - SHA1:dc07575d9d383bfdefgnji239819755e5ef44f [weak]
    - MD5Sum:3f0a5f1e283914818aaa044ceb3d [weak]
   Hashes of received file:
    - SHA256:614d04fa59f6f2541e8ddcc320baa8eajfsklf978dc3283911f0cca3516a98e7
    - SHA1:23bhkgcca9d2f334dsjfnjke7285ecdfd11b1c74 [weak]
    - MD5Sum:23nj4k3fjkower3a97509ac5c1720cc2 [weak]
    - Filesize:1097184 [weak]
   Last modification reported: Sun, 16 Aug 2020 00:53:49 +0000
   Release file created at: Mon, 17 Aug 2020 06:50:31 +0000
E: Some index files failed to download. They have been ignored, or old ones used instead.
```

---

```shell
sudo apt-get update -o Acquire::CompressionTypes::Order::=gz
sudo apt-get upgrade -y
sudo apt-get update
```

---

```shell
sudo vi /etc/apt/sources.list
```

```shell
:%s/kr.archive.ubuntu.com/ftp.daumkakao.com
```
{: file='vi editor'}

---

# 참고

- **[melonicedlatte 님의 포스팅](https://melonicedlatte.com/2020/08/17/190200.html "[Error solve] apt-get update Hash sum mismatch error")**
[Error solve] apt-get update Hash sum mismatch error

- **[Jade 님의 포스팅](https://blog.ysoft.kr/22 "[Ubuntu] apt update [Some index files ...] 오류 해결방법")**
[Ubuntu] apt update [Some index files ...] 오류 해결방법