---
title: 'Git stash ๋ณต์ํ๊ธฐ'
date: 2020-03-30 14:24:14
category: 'development'
draft: false
---

## ๐ ๋ฐฐ๊ฒฝ

ํ์์ฒ๋ผ stash๋ฅผ popํ๋ค๊ฐ(๋ถ๋ช pop์ด์๋๋ฐ์... vscode ๋ฌด์จ ์ผ์ด์ฃ ...?) stash๊ฐ drop๋๋ ์ฐธ์ฌ(...)๋ฅผ ์ ์ ๊ฒช์์ต๋๋ค.
์์ผ๋ก stash apply๋ฅผ ์ํํํ๋๋ก ํด์ผ๊ฒ ์ต๋๋ค. ๐

## ๐ฅ ๋ฌธ์ 

Git ์ฌ์ฉ ์ค stash๋ฅผ ์ค์๋ก dropํ๋ ๊ฒฝ์ฐ, ํน์ drop ํ ๋ค์ ์ ์ฉํด์ผ ํ๋ ๊ฒฝ์ฐ๊ฐ ์์ต๋๋ค.

## โ๏ธ ํด๊ฒฐ

-   ๋จผ์  ๋ค์๊ณผ ๊ฐ์ด ์๋ ฅํด hash ๊ฐ์ ๊ฒ์ํฉ๋๋ค.

```bash
$ git fsck --no-reflog | awk '/dangling commit/ {print $3}'
```

-   git show ๋ช๋ น์ด๋ฅผ ์ด์ฉํด ๋๋๋ฆฌ๊ณ  ์ถ์ ์์์ด ๋ง๋์ง ํ์ธํ  ์ ์์ต๋๋ค.

```bash
$ git show YOUR_HASH
```

-   gitk ๋ช๋ น์ด๋ฅผ ์ด์ฉํด ๊ฒ์ํ๋ ๋ฐฉ๋ฒ๋ ์์ต๋๋ค.

```bash
$ gitk --all $( git fsck --no-reflog | awk '/dangling commit/ {print $3}' )
```

-   ํด๋น hash ๊ฐ์ ์ฐพ์ ๋ค์ stash๋ฅผ applyํฉ๋๋ค.

```bash
$ git stash apply YOUR_HASH
```
