````markdown
---
sidebar_position: 1
---

# 튜토리얼 소개

이 페이지에서는 **5분 이내에 Docusaurus를 알아보는 방법**을 안내합니다.

## 시작하기

새 사이트를 **생성**하여 시작하세요.

또는 **지금 바로 Docusaurus를 사용해 보려면** **[docusaurus.new](https://docusaurus.new)** 를 이용하세요.

### 준비물

- [Node.js](https://nodejs.org/ko/download/) 버전 20.0 이상

  - Node.js 설치 시 필요한 종속성 관련 체크박스를 모두 선택하는 것을 권장합니다.

## 새 사이트 생성

다음 명령으로 classic 템플릿을 사용하여 새 Docusaurus 사이트를 생성합니다:

```bash
npm init docusaurus@latest my-website classic
```

이 명령은 프로젝트에 필요한 템플릿과 의존성을 자동으로 설치합니다.

## 사이트 시작

개발 서버를 실행합니다:

```bash
cd my-website
npm run start
```

브라우저에서 http://localhost:3000/ 을 열면 로컬로 실행된 사이트를 볼 수 있습니다.

`docs/intro.md`(이 페이지)를 열어 몇 줄 편집하면 사이트가 **자동으로 다시 로드**되어 변경 사항을 즉시 확인할 수 있습니다.
````
