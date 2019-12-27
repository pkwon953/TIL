# 키워드

web 조건 두가지 - validate, well - formed

get 방식 -

post 방식 - 

urlib - url 작업을 위한 여러 모듈을 모은 패키지

urlib.request - url 주소의 문서를 열고 읽기 위해 사용하는 모듈

urlib.parser - url 주소의 문서를 구문 분석을 위해 사용

응답코드 - 200 OK, 404 Not Found, 500 Server Error

urlib.error - urlib.request에 의해 발생되는 예외를 포함하고 있는 모듈

urlib.parser.urlencode(파라미터) - url 요청 / 파라미터를 인코딩 함수

urlib.request.urlretrieved(url, 로컬에 저장될 파일 이름) - url 주소의 문서를 다운로드해서 로컬 저장

requests 모듈 - 간편하게 HTTP request 보내고 세션 유지 용이, 파라미터 데이터들을 편리하게 

get() , post(), put(), delete()

get(url, headers=,cookies=) 함수로부터 반환 객체 - Response 객체

Response객체.request - 요청을 보낸 객체(request객체)에 접근

Response객체.status_code - 요청에 대한 응답 코드

Response객체.text - 요청에 대한 응답 body내용을 text 변환

Response객체.content - 요청에 대한 응답 body내용을 byte 변환

Response객체.raise_for_status() - 에러 발생(200 OK 응답이 아닌 경우)

Response객체.json()  - 요청에 대한 응답이 JSON의 경우 딕셔너리 형태로 변환

BeautifulSoup - HTML, XML 파싱하는데 사용되는 라이브러리

BeautifulSoup( ,Parser) - 생성자 함수에 문서 객체(string, url)를 인수로 전달해서 파싱 객체 생성

html.parser - 단순한 html 문서 파싱하는 구문 분석

lxml.parser - html, xml에 대해 더 유연하고 빠르게 구문 분석 

xml.parser - xml 문서만 구문분석

html5lib - 구조가 복잡한 html 문서 구문분석

bs.parent.child.grandchild ....방식의 계층 구조로 구성된 html 문서 특정 요소 접근

bs.find_all(태그명, (속성명: 값...)) - 태그명, 태그와 속성면과 값 등 조건에 맞는 모든 태그를 반환하는 함수

bs.find(태그명, (속성명: 값...)) - 태그명, 태그와 속성면과 값 등 조건에 맞는 하나의 태그를 반환하는 함수

find()등의 함수로부터 반한되는 객체 타입 - bs.element.Tag

bs.element.Tag.attrs - 속성으로부터 태그의 모든 속성 추출

[태그의 내용 추출]

bs.element.Tag.string, text, contents, strings, stripped_strings,get_text()



bs.select() - CSS의 선택자를 조건에 맞는 모든 태그를 반환하는 함수

모든 요소 CSS의 선택자: *

<p id ="p1"></> 태그의 id 선택자 : #p1

<p class ="p1"></> 태그의 class 속성 선택자 : p1



