## Linear Regression
![image](https://user-images.githubusercontent.com/55045082/91530446-0b9c5a00-e946-11ea-8c12-3c6ac4244237.png)
* Linear Regression  
: label의 범위가 넓은 데이터가 어떤 label로 분류될지 예측하는 것이다.
 * Linear Hypothesis  
 : 선형적인(Linear) 데이터 모델이 training set에 적용될 것이라는 가설이다.  
![image](https://user-images.githubusercontent.com/55045082/91530563-4a321480-e946-11ea-8c1b-f8520ae2f849.png)의 형태이며, 변수가 여러 개인 Multi-variable Linear Regression의 경우 변수를 행렬 X로, weight를 행렬 W로 하여  
![image](https://user-images.githubusercontent.com/55045082/91530596-5918c700-e946-11ea-873b-b64b4be5f022.png)
와 같이 표현한다.  
인스턴스가 여러 개인 경우에도 행렬을 이용해 표현한다(상수 ![image](https://user-images.githubusercontent.com/55045082/91530623-646bf280-e946-11ea-8170-cdf0658573a4.png)는 생략).
 * Cost function(=Loss function)  
 : 세운 가설과 실제 데이터가 얼마나 차이 나는지 계산하는 것이다. 실제 데이터와 training set의 거리를 구하는 것으로, 일반화하여 ![image](https://user-images.githubusercontent.com/55045082/91530754-a137e980-e946-11ea-8c80-3a66951a1e04.png)
로 표현한다.
 * Cost 최소화 알고리즘(Gradient Descent Algorithm)  
 : 볼록 함수(convex function) 모양의 cost 함수 그래프의 한 지점에서 시작해 step 당 ![image](https://user-images.githubusercontent.com/55045082/91530899-d7756900-e946-11ea-9967-596e1bdae8a1.png)(learning rate)만큼 ![image](https://user-images.githubusercontent.com/55045082/91530908-db08f000-e946-11ea-8467-232202b1bfe8.png)와 ![image](https://user-images.githubusercontent.com/55045082/91530916-df350d80-e946-11ea-8580-867b58feb86a.png)
를 조금씩 이동시켜 cost를 감소시켜 최소화하는 알고리즘이다(반드시 볼록함수 모양이어야 한다.).  
cost를 최소화하는 ![image](https://user-images.githubusercontent.com/55045082/91530908-db08f000-e946-11ea-8467-232202b1bfe8.png)와 ![image](https://user-images.githubusercontent.com/55045082/91530916-df350d80-e946-11ea-8580-867b58feb86a.png)
를 찾는 것이 Linear Regression의 학습 목표이다.  
Gradient Descent Algorithm의 식은 ![image](https://user-images.githubusercontent.com/55045082/91531002-07bd0780-e947-11ea-8092-036e4c727465.png)인데, 이것을 Linear Regression에 적용하면 ![image](https://user-images.githubusercontent.com/55045082/91531009-0ab7f800-e947-11ea-8eed-abd9474b562f.png)가 된다.
