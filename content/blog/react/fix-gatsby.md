---
title: 'GatsbyJS gatsby develop 에러 해결하기'
date: 2019-9-1 19:06:12
category: 'react'
draft: false
---

## 💥 문제

gatsby develop 실행시 아래와 같은 오류가 발생하는 경우가 있습니다.

```bash
Error: EISDIR: illegal operation on a directory, readlink 'C:\my-default-starter\.cache'
```

## ❗️ 해결

-   먼저 package-lock.json 파일을 삭제합니다.

```bash
$ rm package-lock.json
```

-   그 다음 node_modules 디렉토리를 삭제합니다.

```bash
$ rm -rf node_modules
```

-   .cache와 public 디렉토리도 삭제합니다.

```bash
$ gatsby clean
```

-   모듈 재설치 후 다시 실행합니다.

```bash
$ npm i
$ gatsby develop
```
