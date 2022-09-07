
## 3강 확률변수의 발생
- probabilistic simulation, stochastic simulation
- 확률 변수(random variable)사용
### 확률변수 발생과정
- 1. 난수 U[0,1) 발생
- 2. 확률변수 발생공식 적용
- 3. 확률변수 발생(일양, 균등)

### 연봉 변화(인상률) 0 ~ 10% 의 일양 분포 변환 공식
- 연봉인상률 = (난수발생함수 * (최대예상인상률 - 최저예상인상률 + 1) + 최저인상률) * 0.01(%로 변환)
```
/** pseudocode **/

perinc,//연봉인상률
perhig,//최대예상인상률
perlow,//최저예상인상률

while(year)
```
