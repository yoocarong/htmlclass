# HTML

## HTML Introduction

- HTML : Hyper Text Markup Language

  - Hyper Text : 하이퍼링크로 연결된 웹 문서 => 웹 문서(페이지)
  - Markup Language : 표시 언어

- HTML 표시 내용

  - Web Page의 Contents
    - Text Contents
    - Multimedia Contents : image, video, audio
      - Embed(ed) Contents
  - Web page의 Structure

## HTML Basic

- 기본 구조

※ ` : backtick

```HTML
<!DOCTYPE html>
<html>
  <head>
    웹 문서의 부가정보
  </head>

  <body>
    웹 문서의 내용
  </body>
</html>
```

## HTML Elements

- Tag와 Contents로 구성
- Tag는 시작태그와 종료태그로 구성
  - contents와 종료태그 없이 시작태그만 있는 요소 : 빈요소(Empty Element)

```HTML
<h1>제목</h1>

<br> => 빈 요소(Empty Element)
```

## HTML Attributes

- HTML Tag의 추가정보
- syntax : name="value"
```HTML
<img src="photo.jpg" alt="사진">
```
## Text Contents Element

### Heading
- 제목
- h(heading)
  - h
### Paragraph
- p(Paragraph) : 단락
- hr(Horizontal Rules) : 수평선(단락 구분)
- br(Line Break) : 강제 줄 바꿈
  (※ 강제 공백(Entity Code) : &nbsp; - Non-breaking space)
  (※ & : ampersand)
  - HTML TEXT 줄바꿈, 공백 인식
    - 공백 1칸으로 인식

### HTML List
- 순서없는 목록 : ul, li
- 순서있는 목록 : ol, li
- 설명 목록 : dl, dt, dd

※ 포함관계/중첩관계(Nested Element)
- 포함하는 요소 : 부모요소(Parent), 조상요소(Ancestor)
- 포함되는 요소 : 자식요소(Child), 자손요소(Descendant)
- 이웃하는 요소 : 형제요소(sibling)

### HTML Link

- 하이퍼링크 연결

- a(anchor)
  - href(hypertext reference) attribute : 연결되는 페이지의 주소 정보
  - target attribute
    - target="_blank" : 새탭 열기 설정
  
- Bookmark 기능
  - 목적지에 id attribute를 사용해서 이름 지정
  - a 태그의 href 속성에 "#이름"으로 위치 표시
  
### HTML Table
- 표를 표시
- table(표 영역 표시)
- tr(table row) : 행, 줄
- th(table heading) : 열, 칸 제목
- td(table data) : 열, 칸
※ 향후 웹 접근성 테이블까지 스터디해야함
※ 웹 개발 시 모바일 환경과 PC환경을 모두 고려해야하는데 테이블은 모바일과 호환되기 어려워서 최근 사용 빈도가 줌, 가로의 크기가 변경되는 환경에서 불편함
※ html table generator(https://www.tablesgenerator.com/html_tables#)

## Multimedia Contents

### HTML image

- img : image
- attribute
  - src(source) : 이미지의 파일 경로, 이름
  - alt(altanative) : 대체 텍스트(이미지가 불러올 수 없을 때 대체하여 표시, 웹 접근성에서 활용)
  - muted : 음소거
  - loop : 반복 재생
  - poster : 영상 포스터(대체) 이미지

## Semantic Element

- 영역을 구분하는 Element를 의미있게 사용하는 것

- header : 로고, 로그인/회원가입, 언어변경
- nav(navigation) : gnb(global navigation bar), lnb(local navigation bar)
- section : 웹 페이지의 본문 / 영역 구분
- article : 웹 페이지의 본분 / 독립된 글(내용)
- aside : 부수적인 내용 / 광고, 배너
- footer : 웹 사이트의 위치 정보 / 관련 링크
- figure : 다이어그램 / 이미지 시각 요소
- main : 웹 페이지 본문 전체

## URL / File Path

- URL(Uniform Resource Locator)
```HTML
http://www.naver.com/video/movie.mp4

=>https://도메인네임/상세경로:포트번호

IP 주소 : Internet Protocol 주소 => 인터넷에서 사용하는 실제 주소
Ex) 192.168.0.1 : 0~255까지의 숫자 4개로 구성

도메인 네임 : 영어 단어(줄임말)로 구성되어 있는 식별 이름

도메인 네임 서버(시스템) : 도메인 네임 => IP 주소로 변환

```

- 경로(URL/File Path) 지정 방식
  - root : 해당 경로의 시작 위치
  - 절대 지정 방식
    - 파일 경로의 전체 URL을 표현하는 방식
  - 상대 지정 방식
    - 현재 페이지를 기준으로 일부 URL을 표현하는 방식
    - root 상대 경로 방식 : root를 기준으로 상대적인 URL 표현
  
```HTML
domain : www.abc.com

/(root) - html - index.html
        - images - photo.jpg
절대 방식 : https://www.abc.com/images/photo.jpg
상대 방식(현재페이지 : index.html) : ../images/photo.jpg
root 상대 방식 : /images/photo.jpg
```

## HTML Head

- head element
  - title : 웹사이트 제목(브라우저 탭에 표시)
  - meta : 웹사이트 관련 정보
  - link : css 파일 불러오기
  - style : css 코드 작성
  - script : js 코드 작성 / 파일 불러오기

- meta
  - charset(character set) : 문자 세트, 글자(문자)를 표시하는 방식
  - 종류/개수 => 용량
    - bit : 0/1이 저장되는 공간
    - 1 bit가 저장/표현할 수 있는 개수(가짓수) : 2
    - n bit가 저장/표현할 수 있는 개수(가짓수) : 2의n승
  - UTF-8 : 글자(문자) 표기하는 방식 중 하나
    - 2 byte로 글자를 표시(65536) : 유니코드
    - 영문 1byte로 표현, 한글 2byte로 표시
    - UTF(Universal Coded Character Set + Transformation Format – 8-bit)
  
  - EUC-KR : 한글, 영문 전용 표시 방식

## HTML Block & Inline

- Block
  - 줄바꿈 되어 새 줄에 표시됨
  - 블럭요소는 너비가 가능한 전체가 채워짐
  - 블럭요소, Text, 인라인요소 모두 포함할 수 있음

- Inline
  - 줄바꿈 되지 않고 한 줄에 표시됨
  - 인라인 요소는 너비가 콘텐츠/자식요소에 맞춰짐
  - Text, 인라인요소 포함할 수 있음(블럭 요소는 포함할 수 없음. 단, a 태그는 예외- 모두 포함할 수 있다)

- div(division)
  - 단순히 영역을 구분하거나 그룹핑을 하는 컨테이너 요소
  - 블럭 요소

- span
  - 단순히 영역을 구분하거나 그룹핑을 하는 컨테이너 요소
  - 인라인 요소

## HTML class, id

- 해당 요소에 이름(식별자/identifier) 지정

```HTML
<p class="클래스이름">...</p>
<p id="아이디이름">...</p>
<p>...</p>
```
- class
  - 하나의 웹문서내에서 동일한 이름을 사용할 수 있음
  - 하나의 요소에서 여러 개의 이름을 사용할 수 있음

- id
  - 하나의 웹문서내에서 동이한 이름을 사용할 수 없음
  - 하나의 요소에서 여러 개의 이름을 사용할 수 없음

```HTML
<div class="test import">text</div>
<div class="test">text</div>

<div id="test">text</div>
<div id="test">text</div> //Error

<div class="test import">text</div> //Error
```
- naming 표기법
  - 네이밍할 때 영어 한 단어로만 네이밍을 하기 힘들기 때문에 여러 단어를 연결해서 하게 됨
  - 연결되는 단어를 구분할 수 있도록 표기


```
hello_world:snake case
hello-html-world:kebab case
helloHtmlWorld:camel case 
```

# CSS

## CSS Introduction / Syntax

- Cascading Style Sheet
- 여러 개의 html 파일에 공통 적용

```
Selector(선택자) {
  CSS property:value;
  CSS property:value;
  CSS property:value;  
}
```

## CSS Selector

- simple selector
  - tag
  - class
  - id

```
tag 선택자
h1{
  color:red;
}

class 선택자
.class-name{
  color:blue;
}

id 선택자
#id-name{
  color:green;
}
```

## Cascading(캐스캐이딩) 규칙

- 동일한 대상에 동일한 CSS property가 여러번 적용될 때 제일 나중에 적용된 스타일 위에 나중에 적용된 스타일 덮어 쓰기됨
- 즉, 우선순위에 따라 적용, 아이디가 1 순위
- 아이디 > 클래스 > 태그

- 우선 순위
  - id : 100
  - class : 10
  - tag : 1
