---
title: 'Django에서 Template 코드 반복하기'
date: 2019-11-11 17:05:05
category: 'development'
draft: false
---

## 💥 문제

Django 사용 중 아래와 같이 템플릿 코드를 반복해야 하는 경우가 있습니다.

```html
<ul>
    <li option-value="1">1번째 아이템</li>
    <li option-value="2">2번째 아이템</li>
    <li option-value="3">3번째 아이템</li>
    <li option-value="4">4번째 아이템</li>
    <li option-value="5">5번째 아이템</li>
    /* ... */
    <li option-value="100">100번째 아이템</li>
</ul>
```

## ❗️ 해결

다음과 같이 작성할 수 있습니다.

```html
<ul>
    {% for i in "x"|rjust:"100" %}
    <li option-value="{{ forloop.counter }}">
        {{ forloop.counter }}번째 아이템
    </li>
    {% endfor %}
</ul>
```
