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

python에서 진행했던 split함수와 동일하게 DataFrame에서도 가능하다. 특히, txt 파일 불러올때 붙어있는 경우가 있는데 이를 split하여 list로 형성한다.

### 데이터 그룹 연산

데이터 그룹 연산을 위해 전처리 과정 중에 마무리 작업 중 하나로 각각의 데이터 이어 붙이기, 데이터 분리하기 등이 있다.

#### 데이터 이어 붙이기

 데이터 이어 붙이는 방법에는 크게 merge, join, concatenate의 방법이 있다.

* merge

> ddd

* join

> ddd

* concatenate

```python
pd.concat([DataFrame, Series], axis,keys,name)
```

concat의 함수 인자

object - 이어붙일 pandas 객체이며 필수 인자

axis - 이어붙일 축 방향

join - concat내에 join을 사용 가능하다. 기본값으로 outer 정리를 한다.

join_axes - concat시킬 색인을 리스트로 작성해 지정할 수도 있다.

keys - 계층 색인을 생성하는데 사용된다.

names - 계층 색인의 레벨별 이름 지정이 가능하다.

verify_integrity - 기본값은 False로 중복을 허용한다.

ignore_index - 이어붙인 축의 색인을 유지하지 않고 길이로 새로운 색인을 생성한다.





groupby

pivot_table

```python
df.pivot_table([],index=[],columns='',aggfunc=)
#aggfunc은 default가 mean으로 넘어간다.
```

aggfunc



pitvot_table을 진행시키면 원래 형태인 DataFrame 객체로 반환하지만, groupby를 진행시키면 groupby 객체를 반환한다.

