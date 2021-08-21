---
title: 'cargo 설치하기'
date: 2020-3-17 15:16:16
category: 'development'
draft: false
---

## 📁 LINUX/MAC

-   curl을 이용해 설치합니다.

```bash
$ curl https://sh.rustup.rs -sSf | sh
```

-   옵션을 선택한 후 설치를 진행합니다.

```bash
Current installation options:

   default host triple:
     default toolchain: stable
               profile: default
  modify PATH variable: yes

1) Proceed with installation (default)
2) Customize installation
3) Cancel installation
```

-   버전을 확인합니다.

```bash
$ cargo --version
```

## 📁 Ubuntu

-   cargo를 설치합니다.

```bash
$ sudo apt install cargo
```

-   버전을 확인합니다.

```bash
$ cargo --version
```
