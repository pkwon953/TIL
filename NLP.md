# **NLP(자연어 처리)**

단어의 벡터화를 통한 불연속적인 자연어에 대한 학습.

Count-based

​	단어, 문맥 출현 횟수를 세는 방법.(ex. SVD,HAL)

Predictive method

​	단어에서 문맥 또는 문맥에서 단어를 예측하는 방법.(ex. word2vec)



>  ```python
> count_codePoint('sentence') #단어
>  ```

Word Embedding

빈도수 기반 푠현은 단어간 의미차를 표현 불가.

단어 자체 의미 자체를 다차원 공간에서 벡터화 필요.

​	단어들 사이의 유사도 측정 가능

​	단어들간의 평균 및 연산을 통해 추론 가능

Continuous Bag of Words

보통 sample의 dimension은 row로 나타나는데 bag of words에선 dimension이 column이 된다.