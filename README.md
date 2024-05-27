# Deep-Learning

### Deep Learning, 딥 러닝
- 인공 신경망 (Artificial Neural Network)의 층을 연속적으로 깊게 쌓아올려 데이터를 학습하는 방식을 의미한다.
  
- 인간이 학습하고 기억하는 매커니즘을 모방한 기계학습이다.

- 인간은 학습 시, 뇌에 있는 뉴런이 자극을 받아들여서 일정 자극 이상이 되면, 화학물질을 통해 다른 뉴런과 연결되며 해당 부분이 발달한다.

- 자극이 약하거나 기준치를 넘지 못하면, 뉴런은 연결되지 않는다.

- 입력한 데이터가 활성 함수에서 임계점을 넘게 되면 출력된다.

- 초기 인공 신경망(Perceptron)에서 깊게 층을 쌓아 학습하는 딥 러닝으로 발전한다.

- 딥 러닝은 Input nodes layer,Hidden nodes layer , Output nodes layer, 이렇게 세 가지 층이 존재한다.

---

### SLP(Single Layer Perceptron), 단층 퍼셉트론 , 단일 퍼셉트론  

- 가장 단순한 형태의 신경망으로써, Hidden Layer(은닉층)이 없고, Single Layer로 구성되어 있다.

- 퍼셉트론의 구조는 입력 Feature와 가중치, activation function, 출력 값으로 구성되어 있다.

- 신경 세포에서 신호를 전달하는 축삭돌기의 역할을 퍼셉트론에서는 가중치가 대신하고, 입력 값과 가중치 값은 모두 인공 뉴런(활성함수) 으로 도착한다.

- 가중치의 값이 클수록 해당 입력 값이 중요하다는 뜻이고, 인공뉴런(활성함수)에 도착한 각 입력 값과 가중치 값을 곱한 뒤 전체 합한 값을 구한다.

- 인공뉴런 (활성함수)은 보통 시그모이드 함수와 같은 계단 함수를 사용하여, 합한 값을 확률로 반환하고 이때 임계치를 기준으로 0 또는 1을 출력한다.

- 로지스틱 회귀 모델이 인공 신경망에서는 하나의 인공뉴런으로 볼 수 있다.

- 결과적으로 퍼셉트론은 회귀 모델과 마찬가지로 실제 값과 예측 값의 차이가 최소가 되는 가중치 값을 찾는 과정이 퍼셉트론이 학습하는 과정이다.

- 최초 가중치 값을 설정한 뒤 입력 feature로 예측 값을 계산하고, 실제 값과의 차이를 구한 뒤 이를 줄일 수 있도록 가중치 값을 변경한다.

- 퍼셉트론의 활성화 정도를 편향(bias)으로 조절 할 수 있으며, 편향을 통해 어느정도의 자극을 미리 주고 시작 할 수 있다.

- 만약에 뉴런이 활성화 되기 위해 필요한 자극이 1000이라고 가정하면, 입력 값을 500만 받아도 편향을 2로 주어 1000을 만들 수 있다.

### SGD(Stochastic Gradient Descent), 경사하강법  
- 경사 하강법 방식은 전체 학습 데이터를 기반으로 계산한다. 하지만 입력 데이터가 크고 레이어가 많을 수록 자원이 소모된다.
- 
- 일반적으로 메모리 부족으로 인해 연산이 불가능 하기 때문에, 이를 극복하고자 SGD 방식이 도입 되었다.
- 
- 전체 학습 데이터 중, 단 한 건만 임의로 선택하여 경사하강법을 실시하는 방식을 의미한다.
- 
- 많은 건 수 중에 한 건만 실시하기 때문에, 빠르게 최적점을 찾을 수 있지만 노이즈가 심하다.
- 
- 무작위로 추출된 샘플 데이터에 대해 경사 하강법을 실시 하기 때문에, 진폭이 크고 불안정해 보일 수 있다.
- 
- 일반적으로 사용되지 않고 SGD를 얘기할 때에는 보통 미니 배치 경사 하강법을 의미한다.

### Mini-Batch Gradient Descent, 미니 배치 경사 하강법 
- 전체 학습 데이터 중, 특정 크기(Batch 크기)만큼 임의로 선택해서 경사 하강법을 실시한다. 이 또한 확률적 경사 하강법이다.

- 전체 학습 데이터가 1000건이라고 하고, batch size를 100건이라 가정하면, 전체 데이터를 batch size 만큼 나눠서 가져온 뒤 섞고, 경사 하강법을 계산한다.

- 이 경우 10번 반복해야 1000개의 데이터가 모두 학습 되고 이를 epoch라고 한다. 즉 10 epoch * 100 batch이다.

---  

### Multi Layer Perceptron, 다층 퍼셉트론, 다중 퍼셉트론   
- 보다 복잡한 문제의 해결을 위해서 입력층과 출력층 사이에 은닉층이 포함되어 있다.
- 퍼셉트론을 여러층 쌓은 인공 신경망으로서, 각 층에서는 활성 함수를 통해 입력을 처리한다.
- 층이 깊어질수록 정확한 분류가 가능해지지만, 너무 깊어지면 **Overfitting** 이 발생한다.

### ANN (Artificial Neural Network) 인공신경망 
- 은닉층이 1개일 경우, 이를 인공 신경망이라고 한다.

### DNN (Deep Neural Network), 심층 신경망 
- 은닉층이 2개 이상일 경우 이를 심층 신경망이라고 한다.

### Back-propagation , 역전파  
- 심층 신경망에서 최종 출력(예측)을 하기 위한 식이 생기지만 너무 복잡해지기 때문에 편미분을 진행하기에 한계가 있다.
- 즉 편미분을 통해 가중치 값을 구하고, 경사 하강법을 통해 가중치 값을 업데이트 하며, 손실 함수의 최소값을 찾아야 하는데, 순 방향으로는 복잡한 미분식을 계산할 수 없다.
  따라서 미분의 연쇄 법칙 (Chain Rule)을 사용하여 역방향으로 편미분을 진행한다.

---

### Activation Function, 활성화 함수 
- 인공 신경망에서 입력 값에 가중치를 곱한 뒤 합한 결과를 적용하는 함수이다.
---  
#### 1. 시그모이드 함수 (Sigmoid Function)  
- 은닉층이 아닌 최종 활성화 함수, 즉 출력층에서 사용한다.
- 은닉에서 사용 시, 입력 값이 양의 방향으로 큰 경우일 경우, 출력 값의 변화가 없으며, 음의 방향도 마찬가지이다.
  
  평균이 0이 아니기 때문에 정규 분포 형태가 아니고, 방향에 따라 기울기가 달라져서 탐색 경로가 비효율적(지그재그)이 된다.

#### 2. 소프트맥스 함수 (Softmax Function)  
- 은닉층이 아닌 최종 활성화 함수(출력층) 에서 사용한다.
- 시그모이드와 유사하게 0~1 사이의 값을 출력하지만, 이진 분류가 아닌 다중 분류를 통해 모든 확률 값이 1이 되도록 해준다.
- 여러 개의 타겟 데이터를 분류하는 다중 분류의 최종 활성화 함수(출력층)로 사용된다.

#### 3. 탄젠트 함수  (Tangent Function)
- 은닉층이 아닌 최종 활성화함수(출력층)에서 사용된다.
- 은닉층에서 사용 시, 시그모이드와 달리 -1 ~ 1 사이의 값을 출력해서 평균이 0이 될 수 있지만,

     여전히 입력 값의 양의 방향으로 큰 값일 경우 출력 값의 변화가 미비하고 음의 방향도 마찬가지이다.

#### 4. 렐루 함수 (Relu Function)  
- 대표적인 은닉층의 활성 함수이다.
- 입력 값이 0보다 작으면 출력은 0, 0보다 크면 입력값을 출력하게 된다.

### Cross Entropy  
- 실제 데이터의 확률 분포와, 학습된 모델이 계산한 확률 분포의 차이를 구하는 데 사용된다.
- 분류 문제에서 원-핫 인코딩을 통해 사용할 수 있는 오차 계산법이다.

---  
### Optimizer, 최적화  
- 최적의 경사 하강법을 적용하기 위해 필요하며, 최소값을 찾아가는 방법들을 의미한다.
- loss를 줄이는 방향으로 최소 loss를 보다 빠르고 안정적으로 수렴할 수 있어야 한다.

#### 1. Momentum 
- 가중치를 계속 업데이트 할때마다 이전의 값을 일정 수준 반영 시키면서 새로운 가중치로 업데이트 한다.
- 지역 최소값에서 벗어나지 못하는 문제를 해결 할 수 있으며, 진행했던 방향만큼 추가적으로 더하여 관성처럼 빠져나올 수 있게 해준다.

#### 2. Adagrad (Adaptive Gradient)  
- 가중치 별로 서로 다른 학습률을 동적으로 적용한다.
- 적게 변화된 가중치는 보다 큰 학습률을 적용하고, 많이 변화된 가중치는 보다 작은 학습률을 적용 시킨다.
- 처음에는 큰 보폭으로 이동하다가 최소값에 가까워질 수록 작은 보폭으로 이동하게 된다.
- 과거의 모든 기울기를 사용하기 때문에 학습률이 급격히 감소하여, 분모가 커짐으로써 학습률이 0에 가까워지는 문제가 있다.

#### 3. RMSProp(Root Mean Square Propagation)  
- AdaGrad의 단점을 보완한 기법으로써, 학습률이 지나치게 작아지는 것을 막기 위해 **지수 가중 평균법(exponentially weighted average)** 을 통해 구한다.
- 지수 가중 평균법이란, 데이터의 이동 평균을 구할 때 오래된 데이터가 미치는 영향을 지수적으로 감쇠하도록 하는 방법이다.
- 이전의 기울기들을 똑같이 더해가는 것이 아니라, 훨씬 이전의 기울기는 조금 반영하고 최근의 기울기를 많이 반영한다.
- feature마다 적절한 학습률을 적용하여 효율적인 학습을 진행할 수 있고, AdaGrad 보다 학습을 오래 할 수 있다.

#### 4. Adam (Adaptive Moment Estimation)  
- Momentum과 RMSProp 두 가지 방식을 결합한 형태로써, 진행하던 속도에 관성을 주고, 지수 가중 평균법을 적용한 알고리즘이다.
- 최적화 방법 중에서 가장 많이 사용되는 알고리즘이다.
