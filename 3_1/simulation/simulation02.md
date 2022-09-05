
## 2강 확률적 시뮬레이션
- probabilistic simulation, stochastic simulation
- 확률 변수(random variable)사용
### 확률적 상황
- 실제상황에서 가변적 변수가 있으면 확률 변수로 가정한다.
  > - 일양분포(균등분포), 정규분포, 지수분포 등이 있다
  > - 서울에서 부산까지 KTX 소요시간
  > - 성적분포(정규분포)
  > - 은행에 도착하는 고객의 도착시간 간격 또는 봉사시간(지수분포, 연속적상황)
  > - 하루 동안 발생하는 출생자 수(이산적상황, 1, 2, 3 등 딱 떨어짐)
### 연속형 일양분포
  > 전철을 기다리는 시간, 특정 구간에서 고루 분포되는 값

![image](https://user-images.githubusercontent.com/22282950/188367299-0b51792c-c81c-476b-b5b7-e40ddf7f9874.png)

### 정규분포
  > 수능 점수 등 평균, 표준편차가 뚜렷한 값

![image](https://user-images.githubusercontent.com/22282950/188367061-c874e125-e25d-40ae-913b-fcb13c3e1624.png)

### 지수분포
  > 시간의 간격을 주로 표현
  
![image](https://user-images.githubusercontent.com/22282950/188368702-593897f3-c72d-4db4-bc7e-93ba936ec78d.png)

### 포아송 분포(poission distribution)
  > 출생자 수 등 이산형 값들을 표현

![image](https://user-images.githubusercontent.com/22282950/188368912-4ea6d25e-1cbb-41fb-ab4b-1f2d6aea5df1.png)

### 난수의 개념
  - 발생확률이 같다,
  - 예측할수 없다.
  - 주사위,
  - 난수표기 -> U[0,1)
  - 난수 = 일양 확률변수를 발생시킨다.
