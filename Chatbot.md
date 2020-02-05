# **챗봇(Chatbot)**

---

챗봇 구동하는 3가지 메커니즘(Entity, Intent, Slot filling)

Google Dilogflow를 통해 챗봇 구현하기

> 1. Create Agent
> 2. Intents 생성하기
> 3. System Entity 기본 DEFAULT로 설정되지만, Training phrase에서 drag하면 선택 가능
> 4. Response에서 $를 선택하면 Training phrase에서 만든 System Entity 선택해서 넣어줄 수 있음.
> 5. 기본  Intent에 정의된 목적어 수보다 적게 명령하는 경우, prompts를 통해 필요한 목적어를 얻기 위한 slot filling을 진행한다.
>
>  ※ Fulfillment 
>
>  ※ Integration

어느 부분을 Framework에 두고, Code에 둘 지 결정을 잘해야함.

종속된 Intent 생성

> 1. 이미 생성한 Intents에 Add follow 클릭후 Custom 종속 생성.
> 2. Follow-up intent를 #~~~.entity 형식으로 가지고 온다.
>
>  ※ Intent의$는 전역변수가 아니다. 따라서, 부모 Intent의 context를 가지고 오기 위해서 #을 작성한다.

파라미터 설정하는 방법 - 임의로 파라미터 직접 입력 or system entity 할당

복합 Entity 설정

> 1. Default로 선택된 Define Synonym 해제.
> 2. Entity 2개 작성 설정.

중국집 주문하기 챗봇

> ```python
> import requests
> import json
> 
> def get_answer(text, sessionId):
>     data_send = {
>         'query': text, 'sessionId': sessionId,
>         'lang': 'ko', 'timezone' : 'Asia/Seoul'
>     }
>     data_header = {
>         'Authorization': 'Bearer address',
>         'Content-Type': 'application/json; charset=utf-8'
>     }
>     dialogflow_url = 'https://api.dialogflow.com/v1/query?v=20150910'# 20150910은 API버전
>     #http 프로토콜 구성(주소,헤더, 콘텐트)
>     res = requests.post(dialogflow_url, data=json.dumps(data_send), headers=data_header)
>     #requests.post(주소값,data 딕셔너리를 문자열로 변환하는,헤더 정보(딕셔너리type))
>     if res.status_code == requests.codes.ok:
>        return res.json()    #딕셔너리 값으로 리턴 그 반대인 함수 .dumps()
> #주로 json 사용, xml은 거의 사용 안하지만 환경설정 정도 사용하는 경우 있음.
>     return {}
> 
> dict = get_answer('짜장 , 짬뽕 5개 주세요', 'user01')
> if dict['result']['metadata']['intentName'] == 'order2':
>     price = {"짜장면":5000,"짬뽕":10000,"탕수육":20000}
>     params = dict['result']['parameters']['food_number']
>     
>     output = [food.get("number-integer",1)*price[food["food"]] for food in params]#get 함수를 통해 number-integer가 없으면 default로 1로 설정해준다.
>     print(sum(output))
> ```

**TTS 사용하기**

> ```python
> $ pip install gtts
> from gtts import gTTS
> import IPython.display as ipd #노트북 상에서 음성 읽기
> from IPython.display import HTML #HTML 형식을 노트북 상에 띄우기
> tts = gTTS(text='~~~',lang='ko')
> tts.save('output.mp3')
> ipd.Audio('output.mp3',autoplay=True)
> 
> HTML("""
> <iframe
>     allow="microphone;"
>     width="700"
>     height="860"
>     src="https://console.dialogflow.com/api-client/demo/embedded/youraddress">
> </iframe>
> """)
> ```

**Secure Tunnels(NGROK)**

공인 IP 아니어도 외부에서 접속 가능케 하는 터널 프로그램

방화벽 내부 서버를 외부에서 접속 가능

Nac,Linux, Windows, 모바일 지원





