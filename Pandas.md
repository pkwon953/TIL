# Pandas

pandas에는 Series와 DataFrame 이 두가지 형태의 자료구조가 존재한다. 



## Series

 파이썬에서 생성하는 리스트, 튜플 등과 같은 형태인 1차원 배열 구조를 갖는다.

Series 객체의 특징은 1차 배열에서 값만 갖고있는 것이 아니라 값에 연결된 인덱스 값도 동시에 저장된다. 따라서, 파이썬의 리스트와 달리 인덱싱 값을 지정할 수 있어 원하는 데이터를 찾기 더 편리한 면이 있다.

## Dataframe

Series와는 달리 여러 개의 칼럼으로 구성된 형태로 2차원 배열 구조를 갖는다.

Dataframe을 생성하는 간편한 방법은

```python
import pandas as pd

d = {'col1': [1, 2, 8, 7], 'col2': [3, 4, 5, 0]}
df = pd.DataFrame(d)

```



 dataframe에서 column을  drop할때,

```python
df.drop(column,axis,inplace=True)
#여기서 column 설정해주는 방법
#column = df.columns[num] or df.column[num1:num2]
#column = 'column_name'
```

columns로 처리해서 해당하는 칼럼 숫자로 넘겨 drop 시키거나

이름을 직접 넘긴다.(리스트 컴프리헨션 부분은 추후 공부하면서 추가 기재하도록 한다.)

