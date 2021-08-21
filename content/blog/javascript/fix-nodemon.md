---
title: 'nodemon address already 에러 해결하기'
date: 2019-8-28 17:52:13
category: 'javascript'
draft: false
---

## 💥 문제

nodemon 사용 중 아래와 같은 오류가 발생하는 경우가 있습니다.

```bash
Error: listen EADDRINUSE: address already in use :::3000
```

## ❗️ 해결

-   LINUX/MAC에서는 다음과 같이 입력합니다.

```bash
$ lsof -i tcp:3000
```

-   입력 후 해당 포트에서 실행중인 프로세스들을 확인할 수 있습니다.

```bash
COMMAND  PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
sshd    1554 root    3u  IPv4  12767      0t0  TCP *:ssh (LISTEN)
sshd    1554 root    4u  IPv6  12769      0t0  TCP *:ssh (LISTEN)
```

-   강제 종료할 PID를 확인한 후 다음과 같이 입력합니다.

```bash
$ kill -9 yourPID
```

-   WINDOW에서는 다음과 같이 입력합니다.

```bash
netstat -ano | findstr :3000
```

-   입력 후 해당 포트에서 실행중인 프로세스들을 확인할 수 있습니다.

```bash
  TCP    0.0.0.0:3000           0.0.0.0:0              LISTENING       1928
  TCP    [::]:3000              [::]:0                 LISTENING       1928
```

-   강제 종료할 PID를 확인한 후 다음과 같이 입력합니다.

```bash
tskill yourPID
```
