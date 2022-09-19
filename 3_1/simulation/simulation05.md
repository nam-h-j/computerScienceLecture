## 5강 모델링과 시뮬레이션
### 모델링과 시뮬레이션
- 1.실제시스템 -(모델링)-> 2.모델 -(시뮬레이션)-> 3.시뮬레이터

### 시뮬레이션 모델의 이용범주
- 설명적장치: 시스템이나 문제를 정의
- 분석도구: 한계적 구성요소를 결정
- 설계평가도구: 제안된 해결방안을 종합하고 평가
- 예측도구: 미래의 개발계획을 예측

### 시스템
-  어떤 목적을 위하여 하나 이상 서로 관련된 구성요소들이 결합된 집합.
-  모델 : 시스템을 서술한 것
-  시스텀의 범위 결정 문제
-  외적요인들
  - 포함, 무시, 입력변수

### 모델 설계
- 용이한 경우
  - 물리적 규칙이 이용 가능하다.
  - 도형적 표현이 가능하다.
  - 입력, 출력, 구성요소의 변화가 통제 가능하다.

- 어려운 경우
  - 기본 규칙이 없다.
  - 표현하기 어려운 많은 절차적 요소
  - 랜덤 구성 요소
  - 정량화가 어려운 정책적인 입력
  - 인간의 의사결정이 큰 영향을 주는 경우.

### 모델설계 과정(모델링)
- 구성요소들 간의 관계 표현
  - 모델작성 목적 수립
  - 시스템 영역 확정
  - 모델 상세성 확정
  - 평가척도 및 재설계

### 시뮬레이션 모델의 종류
- 결정적 모델과 확률적 모델
  - 확률변수의 유무에 따라.
    - 결정적모델 : 저축1, 공의 탄성
    - 확률적모델 : 주사위, 저축2
- 정적 모델과 동적 모델
  - 정적모델 : 시간과 무관 (몬테칼로 시뮬레이션, 주사위)
  - 동적모델 : 시간의 흐름에 따라 동적으로 변함
- 이산 모델과 연속 모델
  - 이산적 : 대기행렬
  - 연속적 : 공의 탄성
- 물리적 모델과 수리적 모델 
  - 수리적 모델 : 저축, 공의탄성
  - 물리적 모델 : 클레이, 모델하우스등 축소모형