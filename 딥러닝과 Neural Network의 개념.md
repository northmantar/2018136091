## 딥러닝과 Neural Network의 개념
![image](https://user-images.githubusercontent.com/55045082/91536644-f6c4c400-e94f-11ea-97de-9f304ec6c7a2.png)
* Deep Learning  
: 인간의 신경망을 본뜬 머신러닝 모델로, Machine Learning에 속한다.  
이렇게 만든 인공 신경망을 Artificial Neural Network라고 하며,  
Artificial을 생략하여 Neural Network라고만 하기도 한다.
* (Artificial)Neural Network(= NN)  
: 인공신경망으로, 이 신경망의 뉴런 모델은 가지 돌기로부터 세포체로  
입력 값을 받아들여 일정 수준을 넘어서면 Activation function에 의해  
활성화되어 출력 값을 내보낸다.  
![image](https://user-images.githubusercontent.com/55045082/91536757-2b388000-e950-11ea-8a3d-84c48d1461c2.png)
  * Activation function
    * Sigmoid  
    : NN에서 여러 layer가 연속된 후에 마지막 가설 단계에서 사용하는  
    activation function이다(마지막 단의 출력은 0에서 1 사이여야 하기 때문).
    > * Back Propagation  
    : Chain rule(![image](https://user-images.githubusercontent.com/55045082/91537032-9a15d900-e950-11ea-8e82-7714977f748d.png))을 이용해 예측 값과 실제 값의 오류(cost)를 뒤에서 앞으로  
    전파하여 역으로 weight와 bias를 조절하는 것이다.  
    이는 Sigmoid 함수를 이용하기 때문에 0에서 1 사이의 값을 출력하는 Sigmoid 함수의 특성에 의해  
    layer를 거듭할수록 최종 미분 값이 점점 0에 가까워져 입력이 결과에 미미한 영향을 미치는  
    Vanishing Gradient 문제를 초래할 수 있다.
    * ReLU(= Rectified Linear Unit)  
    : Sigmoid 함수를 이용한 Back Propagation의 단점인 Vanishing Gradient를 해결하기 위해  
    마지막 단을 제외한 연속되는 layer들에 사용한다.
  * Weight의 초기화
  : 최종 미분 값은 weight에 큰 영향을 받기 때문에 적절한 weight의 초기 값을 설정하여야 한다.
    * RBM(= Restricted Boatman Machine)  
    : input과 재생산된 input(output에 의해)을 비교하여 그 차가 최소가 되도록 weight를 조절하는 방법이다.  
    이웃한 두 layer 간 forward(= encode)와 backward(= decode)를 반복해 weight를 학습시키는 방식으로  
    다음 layer들을 차례로 학습시킨다.
    * Xavier/He initialization  
    : RBM보다 좀 더 간단한 방법으로, input과 output을 이용하여 weight를 더 좋은 값으로 만드는 것이다.  
    RBM보다 간단하지만, RBM과 비슷하게 잘 작동한다.
  * Overfitting  
  : NN이 깊어질수록 overfitting 될 확률이 높아진다.  
  layer가 많아질수록 training set으로 실행해보면 오류가 줄어드는 것 같지만,  
  test set으로 실행해보면 오히려 오류가 증가하는 것을 확인할 수 있다.
    * 해결법  
    1. training data의 수를 더 많게 한다.
    2. Regularization
    > * L2 Regularization  
    : ![image](https://user-images.githubusercontent.com/55045082/91537586-8028c600-e951-11ea-9f0c-38e950365320.png)
    > * Dropout  
    : 학습하는 동안 랜덤으로 몇몇 노드들을 비활성화하는 것이다. 실제 모델을 사용할 때에는 Dropout rate를 1로 해야 한다.
    > * Ensemble(앙상블)  
    : 똑같은 형태의 NN을 여러 개 만들어 각각을 학습시켜 결과를 합치는 것으로, 제일 많이 사용된다.
