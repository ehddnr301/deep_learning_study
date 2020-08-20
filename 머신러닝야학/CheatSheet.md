# 1-5

## Supervised learning

- 지도학습
- 필요한것 : 과거의 데이터
- 과거의 데이터 속에서 원인과 결과를 찾아냅니다.

### 모델의 구조

- 원인 : 독립변수
- 결과 : 종속변수

### 모델을 학습

- 데이터로 모델을 학습(fit) 합니다.

### 모델을 활용

- 독립변수를 넣어주면 결과인 종속변수를 예측합니다.

# 6-10

## 준비

- 파일 읽기 : `pd.read_csv('/경로/파일명.csv')`
- shape 확인 : `print(data.shape)`
- 칼럼이름 출력 : `print(data.columns)`
- 맨위 5개 관측치 : `data.head()`

## loss

- 학습이 얼마나 진행되었는지 알려주는 부분입니다.
- 각 학습이 끝날때마다 얼마나 정답에 가까워 지는지 평가하는 부분입니다.
- 0에 가까워 질수록 학습이 잘된 모델이라고 할수있습니다.

# 11-15

- w : Weight
- b : bias

워크북 : [https://docs.google.com/spreadsheets/d/11DAONRZ92ob0T0YRIT5KgU9vNeO28bYNvteu_-fbRV0/edit#gid=0]

## 원핫인코딩

- 원핫 인코딩을 할때 `to_categorical(y, 10)` 라는 tensorflow util을 사용하였는데 
- pandas에서 `get_dummies(y)` 를 사용하면 알아서 구해진다고 한다.