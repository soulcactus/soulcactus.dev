---
title: 'create-react-native-app(CRNA) ์์ํ๊ธฐ'
date: 2019-10-11 12:50:11
category: 'react'
draft: false
---

![](./images/react-native.png)

####

## ๐ create-react-native-app ์ค์น

-   ๋จผ์  create-react-native-app์ ์ ์ญ์ผ๋ก ์ค์นํฉ๋๋ค.

```bash
$ npm i -g create-react-native-app
```

## ๐ ํ๋ก์ ํธ ์์ฑ

-   ๋ค์๊ณผ ๊ฐ์ด ํ๋ก์ ํธ๋ฅผ ์์ฑํฉ๋๋ค.

```bash
$ create-react-native-app my-app
```

## ๐ ํํ๋ฆฟ ์ ํ

-   ํํ๋ฆฟ์ ์ ํํฉ๋๋ค.

```bash
? Choose a template: (Use arrow keys)
  ----- Managed workflow -----
> blank                 a minimal app as clean as an empty canvas
  blank (TypeScript)    same as blank but with TypeScript configuration
  tabs                  several example screens and tabs using react-navigation
  ----- Bare workflow -----
  minimal               bare and minimal, just the essentials to get you started
  minimal (TypeScript)  same as minimal but with TypeScript configuration
```

## ๐ name ์ค์ 

```bash
 {
   "expo": {
     "name": "my-app",
     "slug": "my-app"
   }
 }
```

## ๐ ํ๋ก์ ํธ ์์

-   ์๋ ๋ช๋ น์ด๋ฅผ ์๋ ฅํ๋ฉด ๋ค์๊ณผ ๊ฐ์ด ์คํ๋ฉ๋๋ค.

```bash
$ cd my-app
$ npm start
# open localhost:19002
```

####

![](./images/metro-bundler.png)

####

## ๐ Expo ์ค์น ๋ฐ ์คํ

-   ๋๋ฐ์ด์ค์์ Play Store ํน์ App Store์ ์ ์ํด Expo๋ฅผ ์ค์น ํ QR์ฝ๋๋ฅผ ์ดฌ์ํฉ๋๋ค.

####

![](./images/expo.png)

####

## ๐ค Something went wrong?

-   ๋ค์๊ณผ ๊ฐ์ ์๋ฌ๊ฐ ๋ฐ์ํ๋ ๊ฒฝ์ฐ๊ฐ ์์ต๋๋ค.

####

![](./images/expo-error.png)

####

-   ๋ฐฉํ๋ฒฝ > ๊ณ ๊ธ์ค์  > ์ธ๋ฐ์ด๋ ๊ท์น > ์ ๊ท์น > ํฌํธ๋ฅผ ์ ํํด ๋ค์๊ณผ ๊ฐ์ด ์ ์ฉํฉ๋๋ค.

####

![](./images/firewall-1.png)

####

![](./images/firewall-2.png)

####

-   ipconfig ๋ช๋ น์ด๋ฅผ ์ด์ฉํด ๋ด๋ถ ์์ดํผ ์ฃผ์๋ฅผ ํ์ธ ํ ์๋์ ๊ฐ์ด ์๋ ฅํฉ๋๋ค.

```bash
export REACT_NATIVE_PACKAGER_HOSTNAME=your ip
```

-   npm ์ฌ์คํ ํ Expo๋ฅผ ์คํํด QR ์ฝ๋๋ฅผ ๋ค์ ์ดฌ์ํฉ๋๋ค.

```bash
$ npm start
```
