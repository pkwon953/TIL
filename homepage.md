# **Homepage**



![image-20200206092955676](C:\Users\student\AppData\Roaming\Typora\typora-user-images\image-20200206092955676.png)

1. http는 다운로드 서버이다.(완료후 연결되지 않음.)
2. 대다수의 기능은 브라우저의 기능.

image 포함 홈페이지

> ```html
> <h1>Hello</h1>
> <img src = 'wy.jpg' width=300>
> <!-- 위의 경우에는 2번 웹 요청을 받게 된다. image의 물리적인 주소는 http://~~~/.jpg로 표현되기 때문이다. -->
> ```

동일한 image 여러번 포함시킨 경우.

> ```html
> <h1>Hello</h1>
> <img src = 'wy.jpg' width=300>
> <img src = 'wy.jpg' width=300>
> <img src = 'wy.jpg' width=300>
> <!-- image가 cache로 저장돼 위와 동일한 횟수로 요청된다. 하지만, 파라미터가 다른 경우 물리적인 주소값이 변경되므로 캐시가 남아있지않아 동일한 이미지여도 각각 다른 이미지로 인식하게 된다.-->
> ```



실행 파일은 요청한 파일 다운로드만 진행. 실행은 진행되지 않음