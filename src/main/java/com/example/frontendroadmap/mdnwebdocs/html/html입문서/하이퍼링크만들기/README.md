# 하이퍼링크 만들기

## 하이퍼링크란

웹이 제공하는 가장 흥미로운 혁신 중 하나입니다. 웹을 웹으로 만드는 요소라고 불립니다. 
하이퍼링크를 통해 문서를 다른 문서나 리소스에 연결하거나 문서의 특정 부분에 연결하거나, 웹 주소에서 앱을 사용할 수 있습니다.

## 링크의 구조
텍스트를 a 요소 안에 감싸고 웹 주소를 포함하는 href 속성을 사용하여 생성됩니다.

### title 속성에 부가적인 정보 더하기
페이지에 포함된 정보 또는 웹 사이트에서 주의해야 할 사항 등 링크에 대한 추가 정보를 포함합니다.

### 문서 조각
문서 상단이 아닌 HTML 문서 내부의 특정 부분에 연결할 수 있습니다. 연결하고 싶은 태그에 id 속성을 넣어주면 됩니다.

```html
<h2 id="Mailing_address">Mailing 주소</h2>

<p>
    우리에게 메일을 보내고 싶으시다면,
    <a href="***.html#Mailing_address">메일 주소</a>를 확인해주세요.
</p>
```

같은 원리로 현재 문서의 다른 부분에 연결할 수도 있습니다.

### 절대 URL과 상대 URL
- 절대 URL은 웹에서 정의된 절대적인 위치를 가리킵니다.
- 상대 URL은 연결되어 있는 파일로부터의 상대적인 위치를 가리킵니다.

### 비 HTML 리소스 연결시 명확한 표식 남기기
다운로드 될 리소스에는 혼동을 줄이기 위해 명확한 문구를 추가해야 합니다.

### 다운로드 연결 시 download 속성 사용
브라우저에서 열지 않고 다운로드할 리소스에 연결하는 경우 download 속성을 사용해서 기본 저장 파일 이름을 제공할 수 있습니다.
```html
<a
  href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=en-US"
  download="firefox-latest-64bit-installer.exe">
  Download Latest Firefox for Windows (64-bit) (English, US)
</a>
```

### 이메일 링크
클릭하면 리소스 또는 페이지에 연결하는 대신 새 발신 전자 메일 메시지를 여는 링크 또는 버튼을 만들 수 있습니다. mailto: 스키마를 사용해서 구현하면 됩니다.

세부 사항을 지정하고 싶으면 대표적으로 subject, cc, body를 지정할 수 있습니다.

```html
<a
  href="mailto:nowhere@mozilla.org?cc=name2@rapidtables.com&bcc=name3@rapidtables.com&subject=The%20subject%20of%20the%20email&body=The%20body%20of%20the%20email">
  Send mail with cc, bcc, subject and body
</a>
```






