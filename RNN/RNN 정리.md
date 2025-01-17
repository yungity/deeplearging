#RNN(Recurrent Neural Network) : 순환신경망
=================================================
시계열 데이터를 다룰 때 사용하는 네트워크.

### 단층 퍼셉트론 
- 입력과 출력 사이가 바로 연결되어있는 형태. 공식을 간단히 하면 회귀분석식과 비슷함. 
- 출력을 만들기 위해 입력이 주는 영향의 정도인 가중치를 선위에 표시하고 이를 합산해서 하나의 숫자로 바꾸어줌. 
- 이 숫자는 내가 가지고 있는 입력들을 얘가 표현할 수 있는 범위의 값으로 바꿔주는 것. 

= 입력된 데이터를 내가 원하는 하나의 변수와 동일한 값으로 바꿔주는 선형변환을 시켜주는 역할. 


### 가중치 
- 회귀식에서는 가중치는 숫자들의 모음집인 행렬이 입력 값들을 내가 원하는 차원, 내가 원하는 범위대의 값으로 바꾸어주는 역할. 

### 활성함수 
- 이 때 내가 원하는 변수 수가 너무 많기 때문에 변환함수를 사용함. 
- 변환함수를 뭐를 취하느냐에 따라 숫자가 표현할 수 있는 범위가 달라짐. 
- 기본적인 딥러닝은 지도학습에서 수치형으로 예측하는 것은 회귀분석기법. 
- 회귀의 경우 : 항등함수를 활성함수로 사용하거나 아예 안 씀

### 분류에서의 확성함수 
– 1) 시그모이드 함수 : 0과 1사이 중심값을 기준으로 위,아래로 떨어트림. 

### 히든 레이어 
- 내가 가지고 있는 변수 수가 너무 많을 때 변수 수를 줄이고 각각의 정보를 일부 다 포함하면서 특징들을 모아주는 중간 단계를 거치기 위해 히든 레이어를 씀. 
- 중간층의 역할은 행렬의 형태로 변환을 시켜주어 내가 가지고 있는 각각의 입력 변수들을 다 모여서 하나의 값으로 만들어줌. 
- (이 때 이 w값이 큰 쪽으로 모이게 되는 경향을 가짐.) 이는 머신러닝의 차원 축소 기법인 PCA 기능과 같음. 

### PCA 기능 
- 변수를 줄이는 것이 아니라 차원축소라 해서 내가 가지고 있는 변수의 정보들이 다 포함이 되는데 특정 변수들의 정보들은 많이 들어갈 수 있게 설계. 
- 입력값이 입력되면 w값을 곱해주어 원하는 범위의 값으로 데이터를 떨어트려줌. 입력층을 제외한 히든 층과 아웃풋 층에서는 입력을 어떻게 넘겨줄 거냐에 
따라 한번 더 변환을 취해주게됨. 
- 일정한 범위 안의 값으로 넘겨줄 것인지, 특정값 이하의 값은 넘기지 않고 그 이상만 통과시킬 것인지, 
(RELU나 하이퍼블릭 tanh함수 같은 활성화 함수를 쓸 수 있음. )
이값들을 어떻게 넘겨주냐에 따라 활성화 함수를 취하게 되고 맨 뒤에서는 아웃풋을 어떻게 보낼지에 따라 결정해줌.
+ 선형대수학 배우면 내가 원하는 데이터들을 수치나 수식으로 표현해 행렬을 가지고 이런 관계구조들을 표현하는 것. 이런 것을 선형시스템, 
선형 행렬으로 처리됨.

- w값은 벡터로 표현되고 벡터들의 모음집들이 수식 안에 포함됨. 이런 벡터들을 어떻게 구하느냐에 따라 원하는 영역대로 정보를 만들 수 있음.

### 손실함수 
- RNN과 CNN의 공통적인 부분은 입력은 주어져 있지만 머신러닝이라는 특성상 기계에게 구해달라고 하는 것인데, 알고있는 타겟값(목표값)과 모형을 통해 
나온 예측값 사이 차이가 없는 것이 손실을 발생시키지 않는 것이 이상적인 것. 
- 기본적인 신경망들은 입력의 출력이 주어져있는 상태에서 이 값이 최소가 되게 찾을 것.
