## Recurrent Neural Network(= RNN)
![image](https://user-images.githubusercontent.com/55045082/91539134-d434aa00-e953-11ea-832d-6369d6039450.png)
* Recurrent Neural Network(= RNN)  
: 이전의 연산이 그 다음 연산의 결과에 영향을 미치는 데이터인 Sequence data를 처리한다.  
이전 상태와 입력 벡터를 매개변수로 하는 함수를 통해 새 상태를 구하는 형식으로 구성되어 있다.  
식으로는 ![image](https://user-images.githubusercontent.com/55045082/91539279-080fcf80-e954-11ea-87d0-ca1f1b301fc5.png)와 같이 나타낼 수 있다.  
(![image](https://user-images.githubusercontent.com/55045082/91539283-0b0ac000-e954-11ea-83ec-90957b1ae057.png):새 상태, ![image](https://user-images.githubusercontent.com/55045082/91539288-0e05b080-e954-11ea-826d-bc7b00c94ec1.png):이전 상태, ![image](https://user-images.githubusercontent.com/55045082/91539295-0fcf7400-e954-11ea-8c5c-5dcf206894a7.png):입력 벡터)
  * Vanilla RNN  
  : 기본적인, 가장 단순한 형태의 RNN이다. 함수 ![image](https://user-images.githubusercontent.com/55045082/91539315-15c55500-e954-11ea-9786-12fdca13f7cc.png)로 ![image](https://user-images.githubusercontent.com/55045082/91539324-1827af00-e954-11ea-8e0c-615e2468b0a6.png)를 사용한다.  
  ![image](https://user-images.githubusercontent.com/55045082/91539334-1a8a0900-e954-11ea-9c10-a1d89fa6398f.png)  
  ![image](https://user-images.githubusercontent.com/55045082/91539337-1c53cc80-e954-11ea-86bb-c998cf392520.png)  
+) 현재는 RNN 자체보다 LSTM(= Long Short Term Memory)이나 GRU를 사용한다.
