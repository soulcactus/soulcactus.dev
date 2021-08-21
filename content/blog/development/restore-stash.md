---
title: 'Git stash 복원하기'
date: 2020-03-30 14:24:14
category: 'development'
draft: false
---

## 📝 배경

평소처럼 stash를 pop했다가(분명 pop이었는데요... vscode 무슨 일이죠...?) stash가 drop되는 참사(...)를 잠시 겪었습니다.
앞으로 stash apply를 생활화하도록 해야겠습니다. 😅

## 💥 문제

Git 사용 중 stash를 실수로 drop하는 경우, 혹은 drop 후 다시 적용해야 하는 경우가 있습니다.

## ❗️ 해결

-   먼저 다음과 같이 입력해 hash 값을 검색합니다.

```bash
$ git fsck --no-reflog | awk '/dangling commit/ {print $3}'
```

-   git show 명령어를 이용해 되돌리고 싶은 작업이 맞는지 확인할 수 있습니다.

```bash
$ git show YOUR_HASH
```

-   gitk 명령어를 이용해 검색하는 방법도 있습니다.

```bash
$ gitk --all $( git fsck --no-reflog | awk '/dangling commit/ {print $3}' )
```

-   해당 hash 값을 찾아 다시 stash를 apply합니다.

```bash
$ git stash apply YOUR_HASH
```
