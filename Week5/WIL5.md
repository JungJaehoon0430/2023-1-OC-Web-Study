HTML
2
기본
<!DOCTYPE html>으로 시작
<html>과 </html> 사이에 기술
<head>와 </head> 사이에는 document title, 외부 파일의 참조, 메타데이터의 설정 등이 위치, 브라우저에 표시 X
웹브라우저에 출력되는 모든 요소는 <body>와 </body> 사이에 위치

ex)
<!DOCTYPE html>
<html>
  <head> <!--브라우저 표시 X-->
    <meta charset="utf-8"> <!--문자 인코딩 정의 태그,  utf-8 : 대부분 문자 지원-->
    <title>Hello World</title> <!--요소 제목 지정-->
  </head>
  <body>
    <h1>Hello World</h1>
    <p>안녕하세요! HTML5</p>
  </body>
</html>

4
<html lang="ko"> <!--한국어를 주언어, 영어로 할거면 en-->

style tag
style 요소에는 style 정보 정의
head 안에
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>문서 제목</title>
    <style>
      body {
        background-color: yellow;
        color: blue;
      }
    </style>
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </body>
</html>

link tag
외부 리소스와의 연계 정보를 정의, 주로 HTML과 외부 CSS 파일을 연계
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>문서 제목</title>
    <link rel="stylesheet" href="style.css"><!--rel : 링크된 문서 간의 관계, stylesheet : 외부 스타일 시트와의 관계 / href : 로드할 리소스의 결로 지정--><!--"style.css" 파일에서 CSS 스타일을 로드하여 현재 문서에 적용하는 역할, -->
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </body>
</html>

script tag
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <script>
      document.addEventListener('click', function () {
        alert('Clicked!');
      });
    </script>
  </head><!--클릭 이벤트에 대한 이벤트 리스너 정의, if 한수 실행 'Clicked!'라는 경고창이 표시-> -->
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </body>
</html>

src 어트리뷰트를 사용하면 외부 JavaScript 파일을 로드
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <script src="main.js"></script><!--main.js : js파일 이름, 파일이름.js or 파일이름.ts etc..-->
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </body>
</html>

meta tag(description, keywords, author, 기타 메타데이터 정의)
메타데이터는 브라우저, 검색엔진(keywords) 등에 의해 사용
charset 어트리뷰트는 브라우저가 사용할 문자셋을 정의 - "utf-8" : 대부분의 문자열 지원
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
  </head>
  <body>
    <p>안녕하세요</p>
    <p>Hello</p>
    <p>こんにちは</p>
    <p>你好</p>
    <p>שלום</p>
    <p>สวัสดี</p>
  </body>
</html>

SEO(검색엔진 최적화)를 위해 검색엔진이 사용할 keywords을 정의
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript"><!--kewards HTML, CSS, XML, XHTML, JavaScript 사용한다는 의미-->

웹페이지의 설명을 정의
<meta name="description" content="Web tutorials on HTML and CSS"><!--이름 설명, 내용에 웹페이지 설명-->

웹페이지의 저자을 명기한다.
<meta name="author" content="John Doe">

웹페이지를 30초 마다 Refresh
<meta http-equiv="refresh" content="30"><!--content 값에 refresh(새로고침) 할 초, 실시간 정보를 제공하거나 동적으로 업데이트되는 콘텐츠를 보여주는 데 사용-->

body tag
웹페이지를 구성하는 대부분의 요소가 body 요소 내에 기술
<html>
  <head>
    <meta charset="utf-8">
    <title>문서 제목</title>
  </head>
  <body>
    Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
  </body>
</html>

5
제목 (Headings) 크기:h1>h2>h3>...>h6 볼드체
<!DOCTYPE html>
<html>
  <body>
    <h1>heading 1</h1>
    <h2>heading 2</h2>
    <h3>heading 3</h3>
    <h4>heading 4</h4>
    <h5>heading 5</h5>
    <h6>heading 6</h6>
  </body>
</html>

글자 형태 (Text Formatting) 태그

b : 단순히 볼드체
strong : 볼드체 + 웹 접근성에 기여 + 스크린 리더 사용 시 거센 억양

b : 볼드체
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <b>This text is bold.</b><!--볼드체로, 아래와 같음-->
    <p style="font-weight: bold;">This text is bold.</p>
  </body>
</html>

strong : 볼드체 + 웹 접근성에 기여 + 스크린 리더 사용 시 거센 억양, 웹표준 준수
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <strong>This text is strong.</strong><!--볼드체-->
  </body>
</html>

i : Italic체를 지정(기울여져서 써지는거)
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <i>This text is italic.</i>
    <p style="font-style: italic;">This text is italic.</i>
  </body>
</html>

em : emphasized(강조, 중요한) text를 지정 + Italic체로 표현 + 의미론적(Semantic) 중요성의 의미
<!DOCTYPE html>
<html>
  <body>
    <p>This text is normal.</p>
    <em>This text is emphasized.</em><!--emphasized-->
  </body>
</html>

small : small text
<!DOCTYPE html>
<html>
  <body>
    <h2>HTML <small>Small</small> Formatting</h2>
  </body>
</html>

mark : highlighted text를 지정 형광펜
<!DOCTYPE html>
<html>
  <body>
    <h2>HTML <mark>Marked</mark><!--형광펜으로 칠해짐--> Formatting</h2>
  </body>
</html>

del : deleted (removed) text를 지정 - 글자에 줄 쳐진거
<!DOCTYPE html>
<html>
  <body>
    <p>The del element represents deleted (removed) text.</p>
    <p>My favorite color is <del>blue</del><!--글자에 줄 쳐짐--> red.</p>
  </body>
</html>

ins : inserted (added) text를 지정 : 밑줄(<u>태그는 단순히 밑줄을 긋고 싶을 때 사용하고 <ins>x태그는 새로 추가된 내용을 의미할 때 사용하는 태그입니다.)
<!DOCTYPE html>
<html>
  <body>
    <p>The ins element represent inserted (added) text.</p>
    <p>My favorite <ins>color</ins> is red.</p>
  </body>
</html>

sub / sup : sub 태그는 subscripted(아래에 쓰인) text를 sup 태그는 superscripted(위에 쓰인) text를 지정한다.
<!DOCTYPE html>
<html>
  <body>
    <p>This is <sub>subscripted</sub><!--아래로--> text.</p>
    <p>This is <sup>superscripted</sup><!--위로--> text.</p>
  </body>
</html>

본문 태그

p : 단락 (Paragraphs)을 지정
<!DOCTYPE html>
<html>
  <body>
    <h1>This is a heading.</h1>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
  </body>
</html>

br : br tag는 (강제)개행 (line break)을 지정, br tag는 빈 요소(empty element)로 종료태그 X
<!DOCTYPE html>
<html>
  <body>
    <p>This is<br><!--줄바꿈-->a para<br><!--줄바꿈-->graph with line breaks</p>
  </body>
</html>

HTML에서는 1개 이상의 연속된 공백(space)을 삽입하여도 1개의 공백으로 표시 so 공백 넣을라면 &nbsp;
<!DOCTYPE html>
<html>
  <body>
    <p>This is&nbsp; a para&nbsp; &nbsp; graph</p>
  </body>
</html>

pre : 형식화된(preformatted) text를 지정, pre 태그 내의 content는 작성된 그대로 브라우저에 표시, 약간 코드 나오듯이..?
<!DOCTYPE html>
<html>
  <body>
    <p>HTML은 1개 이상의 연속된 공백(space)과 1개 이상의 연속된 줄바꿈(enter)을 1개의 공백으로 표시한다.</p>
    <pre>
var myArray = [];
console.log(myArray.length); // 0

myArray[1000] = true;  // [ , , ... , , true ]

console.log(myArray.length); // 1001
console.log(myArray[0]);     // undefined
    </pre>
  </body>
</html>

hr : 수평줄 삽입
<!DOCTYPE html>
<html>
  <body>
    <h1>HTML</h1>
    <p>HTML is a language for describing web pages.</p>
    <hr><!--여기 길게 가로줄-->
    <h1>CSS</h1>
    <p>CSS defines how to display HTML elements.</p>
  </body>
</html>

q : 짧은 인용문(quotation) 지정, 브라우저는 인용부호(큰따옴표/quotation marks)로 q 요소 감쌈
<!DOCTYPE html>
<html>
  <body>
    <p>Browsers usually insert quotation marks around the q element.</p>
    <p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
  </body>
</html>
blockquote : 긴 인용문 블록 지정, 브라우저는 blockquote 요소를 들여쓰기한다. css를 이용하여 다양한 style을 적용
<!DOCTYPE html>
<html>
  <body>
    <p>Browsers usually indent blockquote elements.</p>
    <blockquote>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    </blockquote>
  </body>
</html>




CSS

1
CSS는 HTML의 각 요소(Element)의 style(design, layout etc)을 정의하여 화면(Screen) 등에 어떻게 렌더링하면 되는지 브라우저에게 설명하기 위한 언어
HTML는 정보와 구조화, CSS는 styling의 정의
HTML과 CSS는 각자의 문법을 갖는 별개의 언어
CSS 혼자서는 의미 X

셀렉터 (Selector, 선택자) : 스타일을 적용하고자 하는 HTML 요소를 선택

프로퍼티 (Property / 속성) : 셀렉터로 HTML 요소를 선택하고 {} 내에 프로퍼티(속성)와 값을 지정하는 것으로 다양한 style을 정의, 프로퍼티는 표준 스펙으로 이미 지정되어 있는 것을 사용하여야하며 사용자가 임의로 정의 X, 여러 개의 프로퍼티를 연속해서 지정할 수 있으며 세미콜론(;)으로 구분
p {
  color: ...;
  font-size: ...;
}

값 (Value / 속성값) : 셀렉터로 지정한 HTML 요소에 style을 적용하기 위해 프로퍼티를 사용, “키워드”나 “크기 단위” 또는 “색상 표현 단위” 등의 특정 단위로 지정
p {
  color: orange;
  font-size: 16px;
}

연동

Link style : (일반적)HTML에서 외부에 있는 CSS 파일을 로드하는 방식 - 걍 이거 써
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="css/style.css"><!--<link> 태그는 HTML 문서에서 다른 파일을 가져오기 위해 사용, rel 속성은 현재 문서와 가져온 파일 간의 관계를 정의, rel="stylesheet" 속성을 사용하여 가져온 파일이 스타일 시트임을 나타냄--><!--href 속성은 가져올 파일의 경로를 지정, css/style.css 경로를 사용하여 style.css 파일을 가져옴(css파일이름.css)(css 폴더 안에 있어야 함)--><!--style.css 파일을 현재 HTML 문서와 연결하여 문서에 스타일을 적용하는 데 사용-->
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>
css 파일
h1 { color: red; }
p  { background: blue; }

Embedding style : (매우 간단한 웹페이지)HTML 내부에 CSS를 포함시키는 방식, Link style을 사용하는 편이 좋음
<!DOCTYPE html>
<html>
  <head>
    <style>
      h1 { color: red; }
      p  { background: aqua; }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a web page.</p>
  </body>
</html>

Inline style : HTML요소의 style 프로퍼티에 CSS를 기술하는 방식, JavaScript가 동적으로 CSS를 생성할 때 사용하는 경우 있음, but 일반적인 경우 Link style을 사용하는 편이 좋음
<!DOCTYPE html>
<html>
  <body>
    <h1 style="color: red">Hello World</h1>
    <p style="background: aqua">This is a web page.</p>
  </body>
</html>

Reset CSS 사용
모든 웹 브라우저는 디폴트 스타일(브라우저가 내장하고 있는 기본 스타일)을 가지고 있어 CSS가 없어도 작동
웹브라우저에 따라 디폴트 스타일이 상이하고 지원하는 tag나 style도 제각각
Reset CSS는 기본적인 HTML 요소의 CSS를 초기화하는 용도로 사용
*브라우저 별로 제각각인 디폴트 스타일을 하나의 스타일로 통일시켜 주는 역할*

자주 사용되는 Reset CSS
- Eric Meyer’s reset
- normalize.css

Eric Meyer’s reset css(이것을 기준으로 사용자의 CSS를 완성해 나가는 방법은 매우 유용)
/* http://meyerweb.com/eric/tools/css/reset/
  v2.0 | 20110126
  License: none (public domain)
*/

html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed,
figure, figcaption, footer, header, hgroup,
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
  font-size: 100%;
  font: inherit;
  vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure,
footer, header, hgroup, menu, nav, section {
  display: block;
}
body {
  line-height: 1;
}
ol, ul {
  list-style: none;
}
blockquote, q {
  quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
  content: '';
  content: none;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}

2
복수개의 셀렉터를 연속하여 지정할 수 있으며 쉼표( , )로 구분
h1, p { color: red; }

전체 셀렉터 (Universal Selector)
패턴 : *	
Description : HTML 문서 내의 모든 요소를 선택. html 요소를 포함한 모든 요소가 선택. (head 요소도 포함된다)
<!DOCTYPE html>
<html>
<head>
  <style>
    /* 모든 요소를 선택 */
    * { color: red; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div><!--구역 나누는데 사용, 레이아웃 할 때 유용-->
    <p>paragraph 1</p>
    <p>paragraph 2</p>
  </div>
  <p>paragraph 3</p>
</body>
</html>

태그 셀렉터 (Type Selector)
패턴 : 태그명	
Description : 지정된 태그명을 가지는 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* 모든 p 태그 요소를 선택 */
    p { color: red; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div>
    <p>paragraph 1</p>
    <p>paragraph 2</p>
  </div>
  <p>paragraph 3</p>
</body>
</html>

ID 셀렉터 (ID Selector)
패턴 : #id	
Description : 어트리뷰트 값	id 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. id 어트리뷰트 값은 중복될 수 없는 유일한 값이다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* id 어트리뷰트 값이 p1인 요소를 선택 */
    #p1 { color: red; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div class="container">
    <p id="p1">paragraph 1</p>
    <p id="p2">paragraph 2</p>
  </div>
  <p>paragraph 3</p>
</body>
</html>

클래스 셀렉터 (Class Selector)
패턴 : .class
Description : 어트리뷰트 값	class 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. class 어트리뷰트 값은 중복될 수 있다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* class 어트리뷰트 값이 container인 모든 요소를 선택 */
    /* color 어트리뷰트는 자식 요소에 상속된다. */
    .container { color: red; }
    /* not supported in IE */
    #p2 { color: initial; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div class="container">
    <p id="p1">paragraph 1</p><!--빨간색-->
    <p id="p2">paragraph 2</p><!--기본-->
  </div>
  <p>paragraph 3</p>
</body>
</html>
HTML 요소에 class 어트리뷰트 값은 공백으로 구분하여 여러 개 지정
래와 같이 클래스 셀렉터를 사용하여 미리 스타일을 정의해 두고, HTML 요소는 이미 정의되어 있는 클래스를 지정하는 것으로 필요한 스타일을 지정
재사용의 측면에서 유용
<!DOCTYPE html>
<html>
<head>
  <style>
    /* class 어트리뷰트 값이 text-center인 모든 요소를 선택 */
    .text-center { text-align: center; }
    /* class 어트리뷰트 값이 text-large인 모든 요소를 선택 */
    .text-large  { font-size: 200%; }
    /* class 어트리뷰트 값이 text-red인 모든 요소를 선택 */
    .text-red    { color: red; }
    /* class 어트리뷰트 값이 text-blue인 모든 요소를 선택 */
    .text-blue   { color: blue; }
  </style>
</head>
<body>
  <p class="text-center">Center</p>
  <p class="text-large text-red">Large Red</p>
  <p class="text-center text-large text-blue">Center Large Blue</p>
</body>
</html>

어트리뷰트 셀렉터 (Attribute Selector)
패턴 : 셀렉터[어트리뷰트]
Description : 지정된 어트리뷰트를 갖는 모든 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* a 요소 중에 href 어트리뷰트를 갖는 모든 요소 */
    a[href] { color: red; }
  </style>
</head>
<body>
  <a href="http://www.poiemaweb.com">poiemaweb.com</a><br>
  <a href="http://www.google.com" target="_blank">google.com</a><br>
  <a href="http://www.naver.com" target="_top">naver.com</a>
</body>
</html>

패턴 : 셀렉터[어트리뷰트=”값”]
Description : 지정된 어트리뷰트를 가지며 지정된 값과 어트리뷰트의 값이 일치하는 모든 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* a 요소 중에 target 어트리뷰트의 값이 "_blank"인 모든 요소 */
    a[target="_blank"] { color: red; }
  </style>
</head>
<body>
  <a href="http://www.poiemaweb.com">poiemaweb.com</a><br>
  <a href="http://www.google.com" target="_blank">google.com</a><br><!--얘만 빨강-->
  <a href="http://www.naver.com" target="_top">naver.com</a>
</body>
</html>
패턴 : 셀렉터[어트리뷰트~=”값”]	
Description : 지정된 어트리뷰트의 값이 지정된 값을 (공백으로 분리된) 단어로 포함하는 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* h1 요소 중에 title 어트리뷰트 값에 "first"를 단어로 포함하는 요소 */
    h1[title~="first"] { color: red; }
  </style>
</head>
<body>
  <h1 title="heading first">Heading first</h1><!--얘만 빨강-->
  <h1 title="heading-first">Heading-first</h1>
  <h1 title="heading second">Heading second</h1>
  <h1 title="heading third">Heading third</h1>
</body>
</html>

패턴 : 셀렉터[어트리뷰트|=”값”]	
Description : 지정된 어트리뷰트의 값과 일치하거나 지정 어트리뷰트 값 뒤 연이은 하이픈(“값-“)으로 시작하는 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* p 요소 중에 lang 어트리뷰트 값이 "en"과 일치하거나 "en-"로 시작하는 요소 */
    p[lang|="en"] { color: red; }
  </style>
</head>
<body>
  <p lang="en">Hello!</p><!--빨강-->
  <p lang="en-us">Hi!</p><!--빨강-->
  <p lang="en-gb">Ello!</p><!--빨강-->
  <p lang="us">Hi!</p>
  <p lang="no">Hei!</p>
</body>
</html>

패턴 : 셀렉터[어트리뷰트^=”값”]	
Description : 지정된 어트리뷰트 값으로 시작하는 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* a 요소 중에 href 어트리뷰트 값이 "https://"로 시작하는 요소 */
    a[href^="https://"] { color: red; }
  </style>
</head>
<body>
  <a href="https://www.test.com">https://www.test.com</a><br><!--얘만 빨강-->
  <a href="http://www.test.com">http://www.test.com</a>
</body>
</html>

패턴 : 셀렉터[어트리뷰트$=”값”]	
Description : 지정된 어트리뷰트 값으로 끝나는 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* a 요소 중에 href 어트리뷰트 값이 ".html"로 끝나는 요소 */
    a[href$=".html"] { color: red; }
  </style>
</head>
<body>
  <a href="test.html">test.html</a><br><!--얘만 빨강-->
  <a href="test.jsp">test.jsp</a>
</body>
</html>


패턴 : 셀렉터[어트리뷰트*=”값”]	
Description : 지정된 어트리뷰트 값을 포함하는 요소를 선택한다.
<!DOCTYPE html>
<html>
<head>
  <style>
    /* div 요소 중에서 class 어트리뷰트 값에 "test"를 포함하는 요소 */
    div[class*="test"] { color: red; }
    /* div 요소 중에서 class 어트리뷰트 값에 "test"를 단어로 포함하는 요소 */
    div[class~="test"] { background-color: yellow; }
  </style>
</head>
<body>
  <div class="first_test">The first div element.</div><!--빨강-->
  <div class="second">The second div element.</div>
  <div class="test">The third div element.</div><!--빨강, 바탕 노랑-->
  <p class="test">This is some text in a paragraph.</p>
</body>
</html>

복합 셀렉터 (Combinator)

후손 셀렉터 (Descendant Combinator)
셀렉터A 셀렉터B
자신의 1 level 상위에 속하는 요소를 부모 요소, 1 level 하위에 속하는 요소를 자손 요소(자식 요소)
자신보다 n level 하위에 속하는 요소는 후손 요소(하위 요소)
후손 셀렉터는 셀렉터A의 모든 후손(하위) 요소 중 셀렉터B와 일치하는 요소를 선택
<!DOCTYPE html>
<html>
<head>
  <style>
    /* div 요소의 후손요소 중 p 요소 */
    div p { color: red; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div>
    <p>paragraph 1</p><!--빨강-->
    <p>paragraph 2</p><!--빨강-->
    <span><p>paragraph 3</p></span><!--빨강-->
  </div>
  <p>paragraph 4</p>
</body>
</html>

자식 셀렉터 (Child Combinator)
셀렉터A > 셀렉터B
자손 셀렉터는 셀렉터A의 모든 자식 요소 중 셀렉터B와 일치하는 요소를 선택
<!DOCTYPE html>
<html>
<head>
  <style>
    /* div 요소의 자식요소 중 p 요소 */
    div > p { color: red; }
  </style>
</head>
<body>
  <h1>Heading</h1>
  <div>
    <p>paragraph 1</p><!--빨강-->
    <p>paragraph 2</p><!--빨강-->
    <span><p>paragraph 3</p></span>
  </div>
  <p>paragraph 4</p>
</body>
</html>

형제(동위) 셀렉터 (Sibling Combinator)
형제 관계(동위 관계)에서 뒤에 위치하는 요소를 선택할 때 사용

인접 형제 셀렉터(Adjacent Sibling Combinator)
셀렉터A + 셀렉터B
셀렉터A의 형제 요소 중 셀렉터A 바로 뒤에 위치하는 셀렉터B 요소를 선택한다. A와 B 사이에 다른 요소가 존재하면 선택되지 않음
<!DOCTYPE html>
<html>
<head>
  <style>
    /* p 요소의 형제 요소 중에 p 요소 바로 뒤에 위치하는 ul 요소를 선택한다. */
    p + ul { color: red; }
  </style>
</head>
<body>
  <div>A div element.</div>
  <ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>

  <p>The first paragraph.</p>
  <ul><!--정렬되지 않은 목록, 나열 순서 중요하지 않은 목록-->
    <li>Coffee</li><!--항목--> <!--빨강-->
    <li>Tea</li> <!--빨강-->
    <li>Milk</li> <!--빨강-->
  </ul>

  <h2>Another list</h2>
  <ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>
</body>
</html>

일반 형제 셀렉터(General Sibling Combinator)
셀렉터A ~ 셀렉터B
셀렉터A의 형제 요소 중 셀렉터A 뒤에 위치하는 셀렉터B 요소를 모두 선택
<!DOCTYPE html>
<html>
<head>
  <style>
    /* p 요소의 형제 요소 중에 p 요소 뒤에 위치하는 ul 요소를 모두 선택한다.*/
    p ~ ul { color: red; }
  </style>
</head>
<body>
  <div>A div element.</div>
  <ul>
    <li>Coffee</li>
    <li>Tea</li>
    <li>Milk</li>
  </ul>

  <p>The first paragraph.</p>
  <ul>
    <li>Coffee</li><!--빨강-->
    <li>Tea</li><!--빨강-->
    <li>Milk</li><!--빨강-->
  </ul>

  <h2>Another list</h2>
  <ul>
    <li>Coffee</li><!--빨강-->
    <li>Tea</li><!--빨강-->
    <li>Milk</li><!--빨강-->
  </ul>
</body>
</html>

가상 클래스 셀렉터 (Pseudo-Class Selector)
가상 클래스는 요소의 특정 상태에 따라 스타일을 정의할 때 사용
특정 상태 예
-마우스가 올라와 있을때
-링크를 방문했을 때와 아직 방문하지 않았을 때
-포커스가 들어와 있을 때
원래 클래스가 존재하지 않지만 가상 클래스를 임의로 지정하여 선택하는 방법
마침표(.) 대신 콜론(:)을 사용, CSS 표준에 의해 미리 정의된 이름이 있기 때문에 임의의 이름을 사용 X
CSS
selector:pseudo-class {
  property: value;
}
<!DOCTYPE html>
<html>
<head>
  <style>
    /* a 요소가 hover 상태일 때 */
    a:hover { color: red; }
    /* input 요소가 focus 상태일 때 */
    input:focus { background-color: yellow; }
  </style>
</head>
<body>
  <a href="#">Hover me</a><br><br>
  <input type="text" placeholder="focus me">
</body>
</html>

