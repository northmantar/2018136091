## Multinomial Classification(= Softmax Regression)
![image](https://user-images.githubusercontent.com/55045082/91534179-11953980-e94c-11ea-87d2-a379af8a5f7d.png)
* Multinomial Classification(= Softmax Regression)  
: label의 종류가 여러 개인 데이터가 어떤 label로 분류될지 예측하는 것이다.
  * Softmax function  
  : weight의 행렬 W와 변수 행렬 X를 곱하여 logits를 계산하면 0과 1 사이의 값이  
  나오지 않을 수 있기 때문에, softmax 함수로 logits의 각 원소를 0에서 1 사이의 값을  
  가지고 원소의 총합이 1인 확률(![image](https://user-images.githubusercontent.com/55045082/91534382-66d14b00-e94c-11ea-9bab-d58675c02d4f.png) : 예측값)로 변환한다.  
  softmax 함수는 ![image](https://user-images.githubusercontent.com/55045082/91534401-70f34980-e94c-11ea-9f2c-28a6ced93c8f.png)와 같이 표현한다.  
이 함수로 얻은 예측 값(![image](https://user-images.githubusercontent.com/55045082/91534452-85cfdd00-e94c-11ea-86fc-df8b277dd823.png))을 one-hot encoding하여 실제 값(![image](https://user-images.githubusercontent.com/55045082/91534462-89fbfa80-e94c-11ea-85ee-7702229d15f3.png)
)을 구할 수 있다.
    * One-hot encoding  
    : 제일 큰 값은 1로, 나머지는 모두 0으로 만드는 기법이다.
  * Cross-entropy cost function(= Loss function)  
  : 예측 값(![image](https://user-images.githubusercontent.com/55045082/91534509-98e2ad00-e94c-11ea-9b1d-b50516f83250.png))과 실제 값(![image](https://user-images.githubusercontent.com/55045082/91534515-9d0eca80-e94c-11ea-9350-4e4ccf0a29b3.png))의 차이인 ![image](https://user-images.githubusercontent.com/55045082/91534601-bfa0e380-e94c-11ea-85a3-d7ee872acbad.png)를  
  cross-entropy cost function이라고 하며, 이는 하나의 training set에 대한 cost 함수이다.  
  여러 개의 training set에 대한 cost 함수는 ![image](https://user-images.githubusercontent.com/55045082/91534625-caf40f00-e94c-11ea-890e-0b801a52c9ee.png)로 나타낸다.
  * Cost 최소화 알고리즘(Gradient Descent Algorithm)  
  : ![image](https://user-images.githubusercontent.com/55045082/91534653-d6dfd100-e94c-11ea-852e-3739404d45ac.png)로 위의 Multinomial Classification의 cost를 최적화할 수 있다.
