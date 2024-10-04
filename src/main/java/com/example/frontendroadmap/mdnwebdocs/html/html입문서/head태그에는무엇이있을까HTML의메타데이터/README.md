# 개요
head는 웹 브라우저에 표시되지 않습니다. title 같은 페이지나 css 링크, 파비콘, 메타데이터를 포함합니다.

## 제목 달기
h1은 내용물의 제목이나 뉴스의 헤드라인을 표시하기 위해 사용됩니다. title은 HTML 문서 전체의 타이틀을 표현하기 위한 메타데이터입니다.
title 요소는 사이트를 북마크할때 내용물을 추천하는 북마크 이름으로 사용하기도 합니다.

## 메타데이터
데이터를 설명하는 데이터입니다. meta 태크를 통해 HTML에서 공식적으로 메타데이터를 적용하는 방법이 있습니다.

```html
<meta charset="uft-8"/>
```
해당 태그는 허용하는 문자 집합에 대해 표시합니다.

### 저자와 설명을 추가
meta의 많은 요소는 name과 content 속성을 가집니다.
- name: 메타 요소가 어떤 정보의 형태를 가지고 있는지 알려줍니다.
- content: 실제 메타데이터의 컨텐츠입니다.
```html
<meta
  name="description"
  content="The Mozilla Developer Network (MDN) provides
information about Open Web technologies including HTML, CSS, and APIs for both
Web sites and HTML5 Apps. It also documents Mozilla products, like Firefox OS." />
```
다음 메타 태그는 MDN docs 메타 태그입니다. 검색엔진에서 실제 해당 내용을 검색하면 나오는 것을 알 수 있습니다.

### 서브페이지
MDN 홈페이지 링크 아래에 나오는 몇 가지 관련 서브 페이지는 사이트 링크라고 합니다. Google의 웹 마스터 도구에서 구성할 수 있습니다.

### meta 미작동
스팸 발송자들이 키워드 목록에 수백 개의 키워버러니는 악용 사례가 생겨 버렸기 때문에 검색엔진들이 무시하는 meta가 많아졌다

### Open Graph Data
```html
<meta
  property="og:image"
  content="https://developer.mozilla.org/mdn-social-share.png" />
<meta
  property="og:description"
  content="The Mozilla Developer Network (MDN) provides
information about Open Web technologies including HTML, CSS, and APIs for both Web sites
and HTML5 Apps. It also documents Mozilla products, like Firefox OS." />
<meta property="og:title" content="Mozilla Developer Network" />
```
웹 사이트에 더 풍부한 메타 데이터를 제공하기 위해 발명한 메타 데이터 프로토콜입니다. MDN을 페이스북에서 링크하면 이미지와 함께 설명이 나타납니다.
트위터에도 유사한 형태의 독점적인 자체 메타데이터를 가지고 있습니다.

### 맞춤 아이콘 추가하기
인덱스 페이지와 같은 디렉토리에 .ico 포멧의 파일을 저장하고
```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
```
다음과 같은 내용을 head에 추가하면 파비콘을 넣을 수 있습니다.

## HTML에 CSS와 JavaScript 적용하기
<link> 는 항상 문서의 head에 위치합니다. stylesheet는 문서의 스타일 시트임을 나타냅니다.
script는 head에 들어갈 필요가 없습니다. body 바로 앞, 문서 본문의 맨 끝에 넣는 것이 좋습니다.

```html
<link rel="stylesheet" href="my-css-file.css"/>
<script src="my-js-file.js"></script>
```

## 문서의 기본 언어 설정
```html
<html lang="en-US"></html>
```
문서의 언어가 설정되어 있으면 검색 엔진에 의해 효과적으로 색인화된다.

또한 다음과 같이 하위 섹션을 다른 언어로 인식하도록 설정할 수도 있다.
```html
<p>Japanese example: <span lang="jp">ご飯が熱い。</span>.</p>
```
