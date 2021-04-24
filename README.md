# [Kokoa-talk](https://tanficial.github.io/Kokoa_clone) clone project

Kakao Talk HTML, CSS clone coding project through Nomadcoder lecture.

노마드코더 강의를 통해 진행한 카카오톡 HTML, CSS 클론 코딩 프로젝트

https://tanficial.github.io/Kokoa_clone

---

## Development Environment

- Chrome
  - Chrome DevTools
  - Page Ruler Redux
  - Color Picker Plus
- VS Code
  - pritter
  - indent-rainbow
  - Community Material Theme
  - Material Icon Theme
- Git
  - Github
  - github pages

---

## Time Line

- 2021.04.16 : Start
- 2021.04.17 : Create index.html, Status Bar
- 2021.04.18 : Create Login Screen
- 2021.04.19 : Create friends.html, Nav Bar, Screen Header, User Component, Friends Screen, Chats Screen
- 2021.04.20 : Create Find Screen, Open Chat Component, More Screen, icon-row, Settings Screen
- 2021.04.21 : Create Chat Screen, Write Message Bar, Animations, Project Deploy
- 2021.04.22 : Update README

---

## Reference Site

- https://ogp.me/
- https://developer.mozilla.org/ko/
- https://d2.naver.com/helloworld/59361
- https://flukeout.github.io/
- https://flexboxfroggy.com/#ko
- https://cssgridgarden.com/#ko
- https://www.matthewlein.com/tools/ceaser
- https://animista.net/
- https://fontawesome.com/
- https://heroicons.dev/
- https://fonts.google.com/

---

## HTML

### 1. basic

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>
```

- head : 페이지에 관한 정보 작성
- body : 컨텐츠 작성

### 2. meta information

```html
<meta charset="UTF-8" />
<meta http-equiv="X-UA-Compatible" content="IE=edge" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- 부가적인 정보나 메타데이터 작성을 위한 태그
- 검색엔진이나 브라우저가 페이지에 대한 정보를 알게하기 위한 태그
- 다양한 프로퍼티와 값을 이용해 여러가지 정보 설정 가능
- open graph protocol : 페이지의 미리보기를 생성
  - 참고 : https://ogp.me/

### 3. link

```html
<link rel="stylesheet" href="./css/styles.css" />
```

- 외부 문서나 파일을 가져오기 위한 태그

### 4. script

```html
<script
  src="https://kit.fontawesome.com/6478f529f2.js"
  crossorigin="anonymous"
></script>
```

- 스크립트 코드를 html문서 내에 작성할 때 사용
- src 프로퍼티를 이용하여 외부 스크립트 파일을 참조할 수도 있다.

### 5. id & class

```html
<div id="id"></div>
<div class="className"></div>
<div class="className1 className2"></div>
```

- id, class 프로퍼티를 이용
- 자바스크립트나 css에서 해당 요소를 찾아 선택할 때 사용
- id는 반드시 유니크한 요소에 하나만 할당한다.
- class는 여러 요소에 동시에 쓸 때 사용
- class는 띄어쓰기 단위로 한 요소에 동시에 여러개의 클래스 할당 가능

### 7. Form

```html
<form action="./friends.html" method="GET" class="login-form">
  <input
    type="text"
    name="username"
    placeholder="Email or phone number"
    class="login-form__input"
  />
  <input
    type="password"
    name="password"
    placeholder="Password"
    class="login-form__input"
  />
  <input type="submit" class="login-form__submit" value="Log in" />
  <input type="submit" class="login-form__submit" value="Sign up" />
  <a href="#" class="login-form__link">Find Kokoa Account or Password</a>
</form>
```

- input태그로 데이터 입력/전송
  - input 태그 참고 : https://developer.mozilla.org/ko/
- action 속성으로 어디로 전송할 지 입력
- method 속성으로 전송 메소드 선택
  - GET
  - POST
  - PUT
  - DELETE

### 8. Semantic and Non-Semantic

- semantic 태그 : 의미가 있는 태그

  ```html
  <header></header>
  <main></main>
  <footer></footer>
  <aside></aside>
  <nav></nav>
  <h1></h1>
  ```

- non-semantic 태그 : 의미가 없는 태그

  ```html
  <div></div>
  <span></span>
  <p></p>
  ```

### 9. Reference

- 더 많은 태그와 정보는 아래 사이트 참조
- https://developer.mozilla.org/ko/

---

## CSS

### 1. basic

```css
nav {
  position: fixed;
  bottom: 0;
  width: 100%;
  background-color: #f0f0f0;
  border-top: 1px solid rgba(0, 0, 0, 0.2);
}
```

- selector로 대상 요소 지정
- { } 안에 property: value; 형식으로 요소의 속성과 값 지정

### 2. Cascading

- cascading : 위에서 아래로 흐르는, 폭포
- 지정된 많은 스타일 중에 어떤 스타일을 적용시킬지에 대한 원리
- 스타일 지정에는 우선순위가 있고 이에 따라 적용됨

  1. 중요도
  2. 명시도
  3. 소스순서
  4. 상속

- 중요도
  1. 사용자 중요선언
  2. 제작자 중요선언
  3. 제작자 일반선언
  4. 사용자 일반선언
  5. 브라우저 정의
- 명시도
  1. 인라인 스타일 : 태그의 style속성을 이용해 적용한 스타일
  2. id 스타일 : id selector를 이용해 지정한 스타일
  3. class 스타일 : class selector를 이용해 지정한 스타일
  4. 태그 스타일 : 태그 이름을 selector로 이용해 지정한 스타일
- 소스순서
  - 동일한 우선순위를 가질 경우 마지막에 나오는 스타일이 적용된다.
- 상속
  - 일부 속성은 따로 값을 가지지 않을 경우 부모의 값을 상속해 가진다.

### 3. id & class

```html
<div id="id"></div>
<div class="className1"></div>
<div class="className1 className2"></div>
<div class="className1 className2 className3"></div>
```

```css
#id {
}

.className1 {
  color: red;
}

.className1.className2 {
  color: blue;
}

.className3 {
  color: green;
}
```

- #id : 해시태그를 사용해 아이디 지정
- .className : .을 사용해 클래스 지정
- 클래스 2개 이상인 경우 and와 modifier기능 구현 가능

### 4. BEM

```html
<div class="block">
  <div class="block__element"></div>
  <div class="block__element block__element--modifier"></div>
</div>
```

```css
.block {
  background-color: red;
}
.block__element {
  background-color: blue;
}
.block__element--modifier {
  background-color: green;
}
```

- block: 요소를 감싸는 클래스
- block\_\_element : 블록 안에 있는 요소
- block\_\_element--modifier : 기존의 정의한 요소의 속성을 변경할 때 사용하는 변경자

### 5. selector

- tag
- class
- id
- pseudo selector
  - :first-child
  - :last-child
  - :nth-child(num)
  - [property="value"]
    - = : 밸류가 완전히 일치
    - ^= : 어두가 일치
    - $= : 어미가 일치
    - ~= : 일치하는 단어가 있는거(단어임, 띄어쓰기단위)
    - \*= : 중간에 어디든 밸류가 일치하는거
- combinator
  - selector1 selector2: selector1 하위에 있는 모든 selector2 요소
  - selector1 \> selector2: selector1 바로 아래 레벨의 자식 selector2 요소
  - selector1 + selector2: selector1 바로 다음에 있는 형제 selector2요소
  - selector1 ~: selector1 바로 다음에 있는 모든 형제 selector2 요소
- state
  - :active : 클릭한 상태
  - :hover : 포인터 올려논 상태
  - :focus : 입력 가능한 상태
  - :visited : 방문한 링크
  - :focus-within : 하위 요소가 입력 가능한 상태

### 6. padding, margin, border, outline

- padding: border와 content 사이의 공간
- margin: border 바깥 공간
- border : 경계선
- outline : border의 외곽선, 크기에 포함되지 않아 레이아웃에 영향을 끼치지 않음

### 7. color

- #000000
- rgb(0, 0, 0)
- rgba(0, 0, 0, 0)

### 8. variables

```css
:root {
  --black: #000000;
}

span {
  color: var(--black);
}
```

- :root안에 이름과 값을 저장해 사용할 수 있다.
- 속성: var(변수이름); 과 같이 사용한다

### 9. block & inline & inline-block

- display 속성을 이용해 지정
- block: 한줄에 한요소만 나타남
- inline: 너비,높이를 가지지 않음, 한줄에 차례대로 나타남
- inline-block : 한줄에 차례대로 나타나는 block요소

### 10. flex box

```css
div {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
```

- flex-direction: 주축을 지정
- justify-content: 주축 정렬
- align-items: 교차축 정렬
- flex-wrap: 너비 모자랄 때 개행여부 지정

### 11. position

- 위치를 지정하기 위해 사용
- position: fixed;
  - 처음 레이아웃 상에 그려진 위치 그대로 화면에 고정, 스크롤 내려도 화면 그 위치에 고정됨
  - top, left, right, bottom 등으로 위치 조절
  - 레이어가 달라진다고 생각할 것
  - 가장위의 레이어가 됨
- position: relative;
  - 처음 위치를 기준으로 위치 미세 조정
  - top, left, right, bottom으로 조절
- position: absolute;
  - position이 relative인 가장 가까운 부모를 기준으로 위치 조절

### 12. transition

```css
button {
  transition: color 1s ease-in-out, width 2s ease-in-out;
}

button:hover {
  color: yellow;
  width: 100vw;
}
```

- 스타일이 바뀔 때 시간을 줘 변화를 보게할 때 사용
- state가 없는 요소에 붙여야 한다, 없는 쪽에 붙이기
  - state쪽에 붙이면 state상태 해제될 때 적용안됨
  - state 상태로 갈때만 적용할라면 state요소에 붙이기
- state에 명시되어 있는 속성만 적용됨, 바뀌는 거만 적용되니까
- ease-in-out
  - transition으로 변화를 줄 때 빨라졌다 느려졌다를 조절하는거
  - linear, ease-in, ease-out, ease-in-out, ease
  - cubic-bezier(\_\_, \_\_, \_\_, \_\_)로 나만의 ease function 만들 수 있음
  - https://www.matthewlein.com/tools/ceaser

### 13. transform

```css
div {
  transform: rotateY(45deg), translateX(100px);
}
```

- 3D 변환
- 형제 노드에 영향을 주지 않음
- transition과 같이써야 멋있고 의미 있음
- transform: rotateY(45deg) rotateX(30deg);
  - rotateY, rotateX, rotateZ, scaleX, translate 등 아주 많음
  - 여러개 같이 쓸 수 있음
  - 아주 많으니까 mdn 참고

### 14. animation

```css
@keyframes mySimpleAnimation {
  /* 단순 from-to 애니매니이션 */
  from {
    transform: func();
  }
  to {
    transform: func();
  }
}

@keyframes myAnimation {
  /* 진행 상태에 따른 애니매니이션 */
  0% {
    transform: translteX();
  }
  50% {
    transform: translteX();
  }
  100% {
    transform: translteX();
  }
}

div {
  animation: myAnimation 2s ease-in-out infinite;
  /* infinite는 무한 반복 */
}
```

- 임의로 애니메이션 재생시킬 때 사용
- transform 만 아니라 다른 속성들도 넣어서 애니매이션 할 수 있음
- transform 만 쓰는거 추천, 다른 속성 안되는거도 있어서
- forwards : 애니메이션 끝나고 계속 유지
- animation-delay : 애니메이션 실행을 지연시킴
- will-change : 미리 애니메이션 요소를 알려줘서 계산 느리거나 떨리는 걸 방지, 그래픽카드를 이용해 애니메이션 가속화, 브라우저 도와줌

### 15. media querys

```css
@media screen and (max-width: 600px) {
  div {
    background-color: tomato;
  }
}
@media screen and (min-width: 601px) and (max-width: 800px) {
  div {
    background-color: blue;
  }
}
@media screen and (min-width: 801px) and (max-width: 1200px) {
  div {
    background-color: wheat;
  }
}
@media screen and (orientation: landscape) {
  span {
    display: none;
  }
}
```

- css만을 이용해 스크린의 사이즈를 알 수 있는 방법
- 반응형 웹사이트에 사용
- max-width, min-width : 스크린 사이즈에 의한 반응형 웹에 사용
- orientaton : 모바일 디바이스 방향 지정
  - landscape나 portraite을 알 수 있음
- mdn 참고하기!
- media type
  - print : 프린트하고 싶을 때, 인쇄화면 보여주고 싶하고 싶을 때, 인쇄화면 보여주고 싶을 때
  - screen : 스크린에 띄울 때
  - all : 모든 디바이스
  - speech : 안씀
- 반응형 웹 메타태그 꼭 써주기! 꼭! 꼭!

  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  ```

---

## GIT

### 1. command

```
// start
$ git init

// stage info
$ git status

// commit history
$ git log

// staging
$ git add

// commit
$ git commit -m "commit comment"

// last commit edit
// 기존의 커밋 내용 수정
// 현재 스테이지 상태 및 새로운 커밋 메세지 마지막 커밋에 덮어씀
$ git commit -amend

// add cancle
$ git reset HEAD [파일명]

// commit cancle
// HEAD^ : 현재 헤드의 부모, HEAD~3 : 현재 헤드부터 마지막 3개
// commit 취소 후 커밋 내용 스테이징, 워킹 디렉토리 보존
$ git reset --soft HEAD

// commit 취소 후 커밋 내용 unstaged, 워킹 디렉토리 보존, default
$ git reset --mixed HEAD

// commit 취소 후 커밋 내용 unstaged, 워킹 디렉토리 삭제, 주의!!!
$ git reset --hard HEAD

// 원격 저장소에 커밋 내용 저장
$ git push

// 원격에서 마지막 커밋 가져오고 병합
$ git pull

// 원격에서 마지막 커밋 가져오고 병합은 하지 않음
$ git fetch

// 브랜치의 커밋 내용 병합
$ git merge

// 브랜치 생성, 브랜치 목록 조회
$ git branch

// 브랜치 변경
$ git checkout

// 작업하던 내용 stash라는 공간에 임시 저장
// 나중에 꺼내 쓸 수 있음
$ git stash
```

### 2. branch

- 독립된 작업을 하기 위해 생성
- 따로 작업한 브랜치의 내용은 merge를 이용해 통합

### 3. github pages

- github에서 제공하는 static site 무료 배포 서비스
- static site : 백엔드 없이 html, css, javascript로만 이루어진 사이트
- gh-pages라는 브랜치를 생성하고 push하면 배포 완료
- 업데이트 방법

  1. main에 push
  2. 로컬 gh-pages 브랜치에서 원격 main 내용 pull or fetch + merge
  3. 원격 gh-pages 브랜치에 push
  4. 업데이트 완료
