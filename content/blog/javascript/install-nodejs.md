---
title: 'Ubuntu에 NodeJS 설치하기'
date: 2019-8-23 11:44:19
category: 'javascript'
draft: false
---

## 📁 curl 설치

-   먼저 curl 버전을 확인합니다.

```bash
$ curl -V
```

-   curl이 설치되어 있지 않다면 curl을 먼저 설치합니다.

```bash
$ apt-get install curl
```

-   만일 설치 단계에서 오류가 발생한다면 업데이트 후 설치를 진행합니다.

```bash
$ sudo apt-get update
$ sudo apt-get dist-upgrade
```

## 📁 nvm 설치

-   nvm은 node version manager의 약자입니다.

```bash
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
```

-   설치 후 버전을 확인합니다.

```bash
$ nvm --version
```

-   nvm not found가 출력된다면 아래와 같이 입력합니다.

```bash
$ source ~/.bashrc
```

## 📁 NodeJS 설치

-   NodeJS를 설치합니다.

```bash
$ nvm install node
```

-   Node 및 npm 버전을 확인합니다.

```bash
$ node -v
$ npm -v
```

## 📁 패키지(모듈) 설치

-   전역으로 npm 패키지를 설치하려면 아래와 같이 입력합니다.

```bash
$ npm i -g packageName
```

-   프로덕션 배포시 반드시 필요한 패키지는 아래와 같이 입력해 설치합니다.

```bash
$ npm i --save packageName
```

-   개발시 테스트 등을 위해 필요한 패키지는 아래와 같이 입력해 설치합니다.

```bash
$ npm i --save-dev packageName
```
