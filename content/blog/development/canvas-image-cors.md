---
title: 'canvas 내부 이미지 CORS 문제 해결하기'
date: 2020-01-23 14:09:15
category: 'development'
draft: false
---

## 💥 문제

HTML을 canvas로 변환한 다음 blob 데이터로 변환해 이미지 파일로 저장하는 기능이 구현돼 있었는데,
사이트 내부에 포함된 미디어 파일들을 Amazon S3로 옮기면서 canvas 내에 포함된 이미지가 내려받은 이미지 파일에 표시되지 않는 문제가 발생했습니다.

_CORS를 통하지 않고, 다른 origin으로 부터 가져온 데이터들은 canvas에 그려지는 즉시 canvas는 오염됩니다._
_오염된 canvas는 더 이상 안전하지 않은 것으로 여겨지고, canvas 이미지에서 데이터를 가져오려는 어떤 시도든 exception이 발생합니다._(출처: [MDN web doc](https://developer.mozilla.org/ko/docs/Web/HTML/CORS_enabled_image))

일단 서버 설정과 Amazon S3 버킷 설정 등에는 문제가 없었습니다.

이미지 태그에 crossorigin="anonymous"를 추가해 문제가 해결되는 듯했으나, 일부 이미지가 여전히 다운로드한 이미지 파일 내부에 포함되지 않는 것은 물론, 화면에도 표시되지 않는 문제가 추가로 발생했습니다.

## ❗️ 해결

이미지 url에 뒤에 timestamp를 포함하는 방법으로 해결할 수 있었습니다.

```javascript
img.setAttribute('src', `url/timestamp=${new Date().getTime()}`);
```
