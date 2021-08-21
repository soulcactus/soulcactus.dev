---
title: 'GraphQL 소개 및 사용기'
date: 2019-9-2 18:49:08
category: 'development'
draft: false
---

![](./images/graphql-logo.png)

####

이 포스트는 [GraphQL](https://graphql-kr.github.io/) 공식문서를 참고했습니다.

## 📝 배경

최근 [노마드 코더](https://academy.nomadcoders.co)에서 GraphQL 관련 강의인 <q>[GraphQL로 영화 API 만들기](https://academy.nomadcoders.co/courses/enrolled/357405)</q>와 <q>[GraphQL로 영화 웹 앱 만들기](https://academy.nomadcoders.co/courses/enrolled/364948)</q>를 수강했습니다. 사실, 호기심 외에 별다른 학습 계기가 있던 것은 아닙니다. 그래도 간략하게 이유를 꼽자면,

-   뭔진 모르겠지만 여기저기서 핫(?)하다.
-   REST API 및 Redux를 대체할 수 있다는 소문(?)이 있다.
-   GatsbyJS에 탑재(?)돼 있다.
-   Facebook에서 만들었다.(중요)

## 💎 GraphQL이란?

공식문서에 따르면 GraphQL은 API를 위한 쿼리 언어이며 이미 존재하는 데이터로 쿼리를 수행하기 위한 런타임입니다. GraphQL은 API에 있는 데이터에 대한 완벽하고 이해하기 쉬운 설명을 제공하고 클라이언트에게 필요한 것을 정확하게 요청할 수 있는 기능을 제공하며 시간이 지남에 따라 API를 쉽게 진화시키고 강력한 개발자 도구를 지원합니다.

## 💡 GraphQL 특징

-   GraphQL API는 엔드포인트가 아닌 타입과 필드로 구성됩니다.
-   스키마에 새로운 필드와 타입을 추가하는 것만으로 기존 쿼리에 영향을 주지 않고 단일 버전의 API를 사용할 수 있습니다.
-   REST API의 OverFetching 및 UnderFetching 문제를 해결할 수 있습니다.
-   REST API의 GET, POST, DELETE, PUT 메소드 대신 Query, Mutation 통해 쿼리합니다.(URL이 필요하지 않습니다.)

## 📝 사용기

GraphQL의 첫인상은 그다지 좋지 않았습니다. 일단 작명에서 오는 압박감이 좀 있었습니다. Graph...? QL...? 세상에 Query Language라니. 친해지기 어렵겠다고 생각했죠.(지금은 이보다 더 적절할 수 없는 작명이라고 생각합니다.) 또한 REST API 및 Redux를 대체할 수 있다고 하는데, Redux처럼 러닝커브가 살벌하면 어쩌나 싶기도 했고요.

결과적으로는, 정적 사이트 생성기를 이용한 간단한 사이드 프로젝트를 계획 중이었기 때문에 좋은 경험이 됐습니다. Gatsby에 조금 더 친숙해질 수 있을 것 같습니다.

노마드 코더의 동영상 강의는 하루 정도 투자하시면 두 강좌 모두 완강 가능합니다. 러닝커브에 대해 제 주관적인 견해를 말씀드리자면, 아직 제대로 사용한 경험이 없어서 그런지 모르겠지만 어렵지 않은 편에 속했습니다. 직관적이고 재밌습니다. 앞으로 열심히 살펴봐야겠습니다.
