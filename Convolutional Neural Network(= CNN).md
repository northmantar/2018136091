## Convolutional Neural Network(= CNN)
![image](https://user-images.githubusercontent.com/55045082/91538257-85d2db80-e952-11ea-9a49-0df283dcb795.png)
* Convolutional Neural Network(= CNN)  
: 이미지 데이터를 filter로 잘라서 부분마다 처리하여 나중에 결과를 합치는 NN으로,  
매우 deep한 신경망일 경우에는 학습이 어렵다.  
구성은 Convolutional Layer와 ReLU함수, Pooling Layer가 자유롭게 반복되다가 끝에  
Fully Connected Network를 붙여 Softmax Classifier와 연결하여 labeling하도록 되어있다.
  * Convolutional Layer  
  : 이미지의 일부만 처리하여 값(점)을 뽑아내는 filter를 stride 크기만큼 움직여 전체 이미지를 훑는다.  
  output 이미지의 크기는 ![image](https://user-images.githubusercontent.com/55045082/91538459-d6e2cf80-e952-11ea-86ae-49096e622ce7.png)이다.  
  (![image](https://user-images.githubusercontent.com/55045082/91538660-1b6e6b00-e953-11ea-91ed-19550c477715.png):input 이미지의 크기, ![image](https://user-images.githubusercontent.com/55045082/91538663-1dd0c500-e953-11ea-8ce0-a0b7cd68a003.png):필터의 크기)  
  이 layer를 통과하면 ![image](https://user-images.githubusercontent.com/55045082/91538731-39d46680-e953-11ea-8a92-16a5c6ab720f.png) 크기의 activation maps가 생긴다.  
  (![image](https://user-images.githubusercontent.com/55045082/91538633-114c6c80-e953-11ea-9998-6279e415d21b.png):output 이미지의 크기, ![image](https://user-images.githubusercontent.com/55045082/91538620-0b568b80-e953-11ea-8aae-1ecbdc4ed450.png):필터의 개수)
  * ReLU 함수  
  * Pooling Layer(= Sampling)  
  : 이미지를 sampling하는 layer이다.
    * Max Pooling
    : filter를 통해 이미지의 각 부분에서 가장 큰 값만을 추출해내는 것이다.
  * Fully Connected Layer
  : 위의 세 종류의 레이어가 반복되어 만들어진 마지막 출력을 Softmax Classifier와 연결해  
  데이터를 labeling하도록 해준다.
