# **1. HTML**

## 1. 기본

우리가 보는 웹페이지가 어떻게 구조화되어 있는지 브라우저로 알 수 있도록 하는 마크업 언어. ***프로그래밍 언어는 아니다.***

Opening tag와 Closing tag 사이에 Contents로 구성하여 작성함. 

* Opening tag(`<>`) : Element를 포함하여 구성하며 효과 적용이 시작된다.
* Closing tag(`</>`) : / 뒤에 Element를 포함하여 작성한다.
* Content : Element의 내용(Content)
* Element : 위에 언급한 세가지를 합쳐놓은 형태로 HTML의 기본 형태이다.

## 2. 문서의 구조

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
  </head>
  <body>
    <p>This is my page</p>
  </body>
</html>
```



* `<!DOCTYPE html>` : 문서의 형식을 나타내는 것으로 여기서는 html 형태의 문서로 이루어져 있다.
* `<html>` : 다음 html 문서를 작성하기 앞서 필요한 기본 element이다.
* `<head>` : 메타 데이터를 담고 있는 element로 HTML 페이지의 모든 내용을 담고 있다.
* `<meta charset = "utf-8">` : 구성된 문자열이 utf-8 형식으로 인코딩 되어 있다.
* `<title>` : 페이지의 제목을 구성한다.
* `<body>` : 웹페이지 상에 웹 유저가 확인할 수 있는 내용은 다 포함되어 있다.
* `<br>` : html상의 줄바꿈이나 enter키라고 생각하면 된다.

# **2. BeautifulSoup**

python 언어를 통해 html이나 xml 형식의 문서를 python 객체로 변환해주는 모듈로  웹 탐색과 크롤링을 위해 사용한다.



# **3. Flask**

웹서버와 웹어플리케이션 기능이 합쳐져 있는 구조이다.

이미지와 같은 파일을 정적인 파일 불러오기

> ```python
> from flask import Flask ,request ,jsonify
> 
> app = Flask(__name__)
> 
> @app.route('/')
> def home(): 
>       
>     return "hello~~!! <img src=wy.jpg>"
> 
> if __name__ == '__main__':
>     app.run(host='0.0.0.0',port=3000,debug=True)
> ```

html 형식으로 이미지 파일 같은 정적 파일을 불러오게 되는 경우, 다음과 같이 인식하지 못한다.

![image-20200206102651735](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200206102651735.png)

따라서, 정적 파일을 Flask를 작성한 경로 아래 static 폴더를 생성해 그 경로로 저장해서 불러오면 작동이 원활하게 된다.

> ```python
> from flask import Flask ,request ,jsonify
> 
> app = Flask(__name__)
> 
> @app.route('/')
> def home(): 
>       
>     return "hello~~!! <img src=/static/wy.jpg>"
> 
> if __name__ == '__main__':
>     app.run(host='0.0.0.0',port=3000,debug=True)
> ```



