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
  