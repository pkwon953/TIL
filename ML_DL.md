#  **인공지능**

GPU의 도입으로 신속하고 강력한 병렬 처리 성능이 향상돼 인공지능의 성장세가 가팔라졌다.

모든 영역의 데이터가 넘쳐나면서 빅데이터가 인공지능의 성장세에 큰 영향을 주고 있다.

## **머신러닝**

인공지능의 하위 분야로서 알고리즘을 이용해 데이터를 분석하고, 분석을 통해 학습하며, 학습 내용 기반으로 판단,예측을 해주는 방법.

데이터 안에서 규칙을 발견하고 그 규칙을 새로운 데이터에 적용해 결과 도출.

### 머신러닝의 응용분야

* 클래스 분류
* 추천
* 회귀
* 차원 축소 - 시각화나 추출을 통해 데이터의 용량을 줄여 계산을 빠르게 하거나 메모리를 절약할 때 사용.

## 딥러닝

인공신경망 이론(퍼셉트론)을 기반으로 복잡한 비선형 문제를 기계가 스스로 학습하여 해결하는 방법

입력층과 출력층 사이에 다양한 은닉층을 넣어 머신러닝을 수행하는 방법이다.

DNN - 신경망을 3개 이상 중첩

#### **텐서플로(Tensorflow)**

턴서플로는 머신 러닝 작업 속도를 크게 높여준다. 기본적으로 파이썬은 GIL 때문에 하나의 코어만 활용가능하다. 

 이미지에 대한 머신러닝을 진행하게 되면 수많은 파라미터를 처리하는데 단일 프로세스로는 수행하기 어려워진다.  따라서 해결책으로 GPU를 사용하여 처리를 진행한다.

GPU에 맞는 코드를 작성하는 일은 파이썬 인터프리터에 코드 실행하는 것처럼 간단하지 않다. 이러한 이유 때문에 텐서플로를 사용한다.

### **퍼셉트론**

입력값과 활성화 함수를 사용해 출력 값을 다음으로 넘기는 가장 작은 신경망 단위이다.

기존 퍼셉트론과 달리 은닉층을 추가한 형태가 좌표 평면을 왜곡시켜 시그모이드 함수 사용하여 XOR 문제를 해결한다.

* **다층 퍼셉트론**

  은닉층으로 퍼셉트론이 각각 자신의 가중치와 바이어스 값을 보내 최종 값을 출력 적용한다.

* **오차 역전파**

  각 층에 적용한 가중치를 경사하강법을 통해 수정해 새로운 가중치를 역전파해 새로운 가중치를 적용시켜 오차를 최소화시켜 적용한다.

* 
