## Binary Classification(= Logistic Regression)
![image](https://user-images.githubusercontent.com/55045082/91532231-f96feb00-e948-11ea-9ae1-b919575fccb8.png)
* Binary Classification(= Logistic Regression)  
: label이 0 또는 1인 데이터가 어떤 label로 분류될지 예측하는 것이다.
  * Logistic Hypothesis  
  : <img src="https://user-images.githubusercontent.com/55045082/91532557-74d19c80-e949-11ea-8249-297e0634d648.png" width="30%"></img>
의 형태의 Linear Regression의 가설을 사용할 경우  
0보다 작거나 1보다 큰 값이 나올 수 있으므로 Sigmoid 함수를 이용해 가설을 변형하여 사용한다.  
이것을 통해 가설을 변형하면 ![image](https://user-images.githubusercontent.com/55045082/91533097-486a5000-e94a-11ea-86dd-bf1d12ce8168.png) 형태의 가설을 얻을 수 있다.
    * Sigmoid function(=Logistic function)  
    : ![image](https://user-images.githubusercontent.com/55045082/91532654-8d41b700-e949-11ea-9a59-4e2876d4cb30.png)(![image](https://user-images.githubusercontent.com/55045082/91532666-916dd480-e949-11ea-9e81-db6d81dc791d.png)는 생략)라 하면, ![image](https://user-images.githubusercontent.com/55045082/91532674-9468c500-e949-11ea-85c0-a4a10ee0bb6f.png)값에 상관없이 0에서 1 사이의 값만  
    나올 수 있도록 하는 함수이다. ![image](https://user-images.githubusercontent.com/55045082/91532678-9763b580-e949-11ea-826d-2589234dc6d3.png)의 형태를 가진다. 
 * Cost function(=Loss function)  
 : Linear Regression과 동일한 cost 함수를 쓰면 cost 함수의 모양이 매끄럽지 못한  
 볼록 함수 형태가 되므로 바꿔주어야 한다. ![image](https://user-images.githubusercontent.com/55045082/91533330-abf47d80-e94a-11ea-9bf5-8828f0acdd6a.png)라 하자.  
 ![image](https://user-images.githubusercontent.com/55045082/91533384-c4fd2e80-e94a-11ea-8827-ff140f62eb34.png)로, 두 ![image](https://user-images.githubusercontent.com/55045082/91533398-c7f81f00-e94a-11ea-965c-dff9bfb56719.png) 함수 그래프를 이용해 볼록 함수를 만든다.  
이를 정리하면 ![image](https://user-images.githubusercontent.com/55045082/91533414-ccbcd300-e94a-11ea-8dcf-7da3ff93df18.png)가 된다.  
따라서 cost 함수는 ![image](https://user-images.githubusercontent.com/55045082/91533417-cf1f2d00-e94a-11ea-8c97-2226255a7bd7.png)
가 된다.
 * Cost 최소화 알고리즘(Gradient Descent Algorithm)  
 : Gradient Descent Algorithm의 식 ![image](https://user-images.githubusercontent.com/55045082/91533521-fece3500-e94a-11ea-8f41-0cf52c0c6105.png)에 위의 cost 함수를 대입하면  
 Binary Classification의 cost를 최적화하는 식을 구할 수 있다.
