---
title: 'NextJS에 proxy 설정하기'
date: 2021-5-10 17:06:29
category: 'react'
draft: false
---

## 📝 배경

진행하고 있는 프로젝트에서 csrf 토큰을 검증하는데, 로컬에서 작업시 요청하는 api 서버와 도메인이 달라 Set-Cookie로 전달받은 csrf 토큰이 자동으로 cookie에 삽입되지 않는 현상이 있었습니다. 
지난 2020년 2월부터 크롬 브라우저에서는 SameSite=Lax가 기본값으로 변경되었기 때문입니다. 
사실 Set-Cookie 뿐만 아니라 작업시 CORS 등 도메인이 다른 경우 여러가지 문제가 있기 때문에 proxy 설정이 필요합니다.

## ❗️ 해결

CRA의 경우 package.json에 proxy 주소를 추가하는 것으로 간단히 해결할 수 있습니다. next에서는 next.config.js에 rewrites 설정을 추가해야 합니다.

- 먼저 아래와 같이 환경변수를 추가합니다.

```javascript
// .env.local

DESTINATION_URL = 'https://exmaple.com/api/:path*' // backend server api url
SOURCE_PATH = '/api/:path*'
```

- 그런 다음 next 설정을 다음과 같이 변경합니다.

```javascript
// next.config.js

module.exports = {
    async rewrites() {
        if (process.env.NODE_ENV !== 'production') {
            return [
                {
                    destination: process.env.DESTINATION_URL,
                    source: process.env.SOURCE_PATH,
                },
            ];
        }
    },
}
```

자세한 사항은 [공식문서](https://nextjs.org/docs/api-reference/next.config.js/rewrites)를 참고하시기 바랍니다.