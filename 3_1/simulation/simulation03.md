
## 3강 확률변수의 발생
- probabilistic simulation, stochastic simulation
- 확률 변수(random variable)사용
### 확률변수 발생과정
- 1. 난수 U[0,1) 발생
- 2. 확률변수 발생공식 적용
- 3. 확률변수 발생(일양, 균등)

### 연봉 변화(인상률) 0 ~ 10% 의 일양 분포 변환 공식
- 연봉인상률 = (난수발생함수 * (최대예상인상률 - 최저예상인상률 + 1) + 최저인상률) * 0.01(%로 변환)
``` c++
/** pseudocode **/
/** 30년간 10퍼센트 저축액 시뮬레이션 **/ 

perinc = 0 //연봉인상률
perhig = 10 //최대예상인상률
perlow = 0 //최저예상인상률
perint = 3 //이율
year = 0 //저축햇수
savings = 0 //저축액

while(year < 30)
do{
//햇수 증가
year = year + 1 

//저축액 = 기존 저축액 + (이율 * 기존저축액) + (0.10 * 연봉)
savings = savings + perint * savings + 0.10 * salary

//연봉인상율 확률변수
call random(seed, U) //난수 발생함수

//난수 범위 지정, 
//마지막에 + 1을 하는 이유는 범위 최대 값은 난수 범위에 포함되지 않기 때문에 포함시키기 위해서 1을 더해줌
//int로 타입을 지정해야 정수형으로 나오기 때문에 이산적인 값으로 난수가 생성됨
perinc = int(U * (perhig - perlow) + 1)
//퍼센트 값으로 변경
perinc = perinc * 0.01

//연봉 인상률 적용
salary = salary + perinc * salary

//결과 출력
print year, salary, savings
}
```
