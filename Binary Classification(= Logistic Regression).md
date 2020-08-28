## Binary Classification(= Logistic Regression)
![image](https://user-images.githubusercontent.com/55045082/91532231-f96feb00-e948-11ea-9ae1-b919575fccb8.png)
* Binary Classification(= Logistic Regression)  
: label이 0 또는 1인 데이터가 어떤 label로 분류될지 예측하는 것이다.
  * Logistic Hypothesis  
  : ![image](https://user-images.githubusercontent.com/55045082/91532557-74d19c80-e949-11ea-8249-297e0634d648.png)
의 형태의 Linear Regression의 가설을 사용할 경우  
0보다 작거나 1보다 큰 값이 나올 수 있으므로 Sigmoid 함수를 이용해 가설을 변형하여 사용한다.  
이것을 통해 가설을 변형하면 형태의 가설을 얻을 수 있다.
    * Sigmoid function(=Logistic function)  
    : ![image](https://user-images.githubusercontent.com/55045082/91532654-8d41b700-e949-11ea-9a59-4e2876d4cb30.png)(![image](https://user-images.githubusercontent.com/55045082/91532666-916dd480-e949-11ea-9e81-db6d81dc791d.png)는 생략)라 하면, ![image](https://user-images.githubusercontent.com/55045082/91532674-9468c500-e949-11ea-85c0-a4a10ee0bb6f.png)값에 상관없이 0에서 1 사이의 값만  
    나올 수 있도록 하는 함수이다. ![image](https://user-images.githubusercontent.com/55045082/91532678-9763b580-e949-11ea-826d-2589234dc6d3.png)의 형태를 가진다. 
