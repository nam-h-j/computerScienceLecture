## 4강 시뮬레이션 응용문제
### 단일창구 대기행렬 문제
- 주유소 시뮬레이션
  - 조건
    - 주유대(창구): 1대
    - 고객도착 상황 : 평균 15명/h 일양분포(=15/60분)
    - 봉사시간 : 평균 4분(Poisson)
  - 문제
    - 평균 대기행렬(Queue)의 길이는?
  - 변수설정
    - arrive //고객이 도착함 (평균 15분/h 일양분포)
    - queue //대기열
    - tpump //소요시간 (평균 4분 포아송분포)

### 포아송분포
```c++
//포아송 알고리즘
void poissn(long *np, float mean, int *pp){
  float prod, b, u;
  *pp = 0;
  b = exp(-mean);
  prod = 1;
  random(np, &u);
  prod = prod * u;
  while(prod >= b)
  {
    random(np, &u);
    prod=prod*u;
    ++(*pp);
  }
}
```

### 고객의 도착
- 평균 15명/h, 일양확률변수(전 구간에서 고르게 분포)
```c++
//pseudo code
call random(U)
if U < 0.25*1 then
  arrive = 1
  queue = queue + arrive //도착한 고객의 대기열
  totarr = totarr + 1 //도착한 총 고객수
```
### 봉사시간
- 평균 4분, 포아송확률변수
```c++
//pseudo code
// 봉사시간과 대기열 조건을 검사
if tpump = 0 and queue != 0 then
{
  queue = queue-1
} 
mean = 4 //평균 분
call poissn(seed, mean, p) //seed : 초기값, mean : 평균시간, p : 포아송 확률 식에서 n 값
tpump = p //봉사시간
```

### 고객의 출발
- 평균 4명, 포아송분포
```c++
//pseudo code
if tpump = 0 and queue != 0 then
{
  queue = queue - 1
  call poissn(seed, mean, p)
  tpump = p
}
```

### 전체 알고리즘
```c++
//변수
read 
tstep, //시뮬레이션 진행 단위 (1분)
prarr, //고객이 도착하는 확률(0.25)
seed, //포아송 난수(임의의 숫자)
mean // 포아송분포 평균시간 (4분)
queue = 0
totque = 0
totarr = 8
tpump = 0
time = 0
tlimit = 100 //총 시뮬레이션 시간

while time < tlimit do
{
  time = time + tstep
  arrive = 0
  call random(seed, U)
  if U < prarr * tstep then //고객 도착
  {
    arrive = 1
    queue = queue + arrive
    totarr = totarr + 1
  }
  if tpump > 0 then //남은 봉사시간
  {
    tpump = tpump - tstep
    if tpump < 0 then
    tpump = 0
  }
  if tpump = 0 and queue != 0 then //고객 출발
  {
    queue = queue - 1
    call poissn(seed, meanm p)
    tpump - p
  }
  totque = totque + queue
}
aveque = totque/(tlimit/tstep)
print aveque, totarr

stop
```
