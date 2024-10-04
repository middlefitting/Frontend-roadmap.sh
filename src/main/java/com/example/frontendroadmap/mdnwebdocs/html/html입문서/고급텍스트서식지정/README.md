# 고급 텍스트 서식 지정

## 설명 목록
설명 목록은 리스트와 다르게 dl 태그를 사용합니다.
각 용어는 dt, 각 설명은 dd를 사용합니다.

### 하나의 용어에 대한 다중설명
하나에 용어에는 열 설명이 포함될 수 있습니다.

## 인용구
HTML에는 인용구 표시에 사용할 수 있는 요소가 존재합니다. 인라인 요소인지에 따라 다르게 표시됩니다.

### 블록 인용구
blockquote 요소로 감싸고 cite 속성에 출처를 표기합니다.

```html
<p>
  <strong>HTML <code>&lt;blockquote&gt;</code> 요소</strong> (또는
  <em>HTML 인용 블록 요소</em>)는 안쪽의 텍스트가 긴 인용문임을 나타냅니다.
</p>

<p>다음은 블록 인용구입니다.</p>
<blockquote
        cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/blockquote">
    <p>
        <strong>HTML <code>&lt;blockquote&gt;</code> 요소</strong> (또는
        <em>HTML 인용 블록 요소</em>)는 안쪽의 텍스트가 긴 인용문임을 나타냅니다.
    </p>
</blockquote>
```

### 인라인 인용구
인라인 인용구는 q 요소를 사용한다는 점만 제외하면 블록 인용구와 동일하게 작동합니다

### 인용
페이지에서 인용 출처를 화면에 나타나게 하고 싶다면 링크나 다른 적절한 방법을 통해 텍스트에서 볼 수 있게 만들어야 합니다.
```html
<p>
  <a href="/ko/docs/Web/HTML/Element/blockquote">
    <cite>MDN 블록 인용구 페이지</cite></a>에 따르면
</p>

<blockquote
  cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/blockquote">
  <p>
    <strong>HTML <code>&lt;blockquote&gt;</code> 요소</strong> (또는
    <em>HTML 인용 블록 요소</em>)는 안쪽의 텍스트가 긴 인용문임을 나타냅니다.
  </p>
</blockquote>

<p>
  인용구 요소 — <code>&lt;q&gt;</code> — 는
  <q cite="https://developer.mozilla.org/ko/docs/Web/HTML/Element/q">
    단락 나누기가 필요 없는 짧은 인용구를 위한 것입니다.
  </q>
  — <a href="/ko/docs/Web/HTML/Element/q"><cite>MDN q 페이지</cite></a>.
</p>
```
인용은 기본적으로 이탤릭체로 스타일이 지정됩니다.

## 약어
약어 또는 약어를 둘러싸는데 사용되는 abbr이 있습니다.
```html
<p>
  웹 문서를 구성하는 데는 하이퍼텍스트 마크업 언어인 <abbr>HTML</abbr>을
  사용합니다.
</p>

<p>
  제 생각에는 그린 <abbr title="목사">목사</abbr>가 전기톱으로 부엌에서 한 것
  같아요.
</p>
```

## 연락처 세부 사항 표시
address 요소를 이용해서 연락처 세부 정보를 표시할 수 있습니다.
```html
<address>
  <p>
    크리스 밀스<br />
    맨체스터<br />
    그림노스<br />
    영국
  </p>

  <ul>
    <li>전화: 01234 567 890</li>
    <li>이메일: me@grim-north.co.uk</li>
  </ul>
</address>
```

## 위 첨자와 아래 첨자
sup와 sub 요소들을 활용할 수 있습니다.
sup는 지수를 나타내고 sub는 밑을 나타냅니다.
```html
<p>My birthday is on the 25<sup>th</sup> of May 2001.</p>
<p>
  Caffeine's chemical formula is
  C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub>.
</p>
<p>If x<sup>2</sup> is 9, x must equal 3 or -3.</p>
```

## 컴퓨터 코드를 나타내기
- code: 일반적인 컴퓨터 코드를 표시합니다.
- pre: 공백(코드 블록)을 유지하기 위해 사용합니다. 여러 공백을 이어써도 텍스트 편집기에서 보는 것과 같이 렌더링됩니다.
- var: 변수 이름을 명확하게 표시합니다.
- kbd: 컴퓨터에 입력 된 키보드 입력을 표시합니다.
- samp: 컴퓨터 프로그램의 출력을 표시합니다.

## 시간과 날짜 표시
기계가 읽을 수 있는 형식으로 시간과 날짜를 표시하기 위한 time 요소를 제공합니다.
```html
<!-- Standard simple date -->
<time datetime="2016-01-20">20 January 2016</time>
<!-- Just year and month -->
<time datetime="2016-01">January 2016</time>
<!-- Just month and day -->
<time datetime="01-20">20 January</time>
<!-- Just time, hours and minutes -->
<time datetime="19:30">19:30</time>
<!-- You can do seconds and milliseconds too! -->
<time datetime="19:30:01.856">19:30:01.856</time>
<!-- Date and time -->
<time datetime="2016-01-20T19:30">7.30pm, 20 January 2016</time>
<!-- Date and time with timezone offset -->
<time datetime="2016-01-20T19:30+01:00">
  7.30pm, 20 January 2016 is 8.30pm in France
</time>
<!-- Calling out a specific week number -->
<time datetime="2016-W04">The fourth week of 2016</time>
```

