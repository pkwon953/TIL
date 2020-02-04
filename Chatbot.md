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

Dialogflow Python으로 가져오기

> 1. OPEN API 가져오는 방식
> 2. 