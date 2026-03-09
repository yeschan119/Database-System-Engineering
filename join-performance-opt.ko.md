# Case Study: Join Performance Optimization

## Context

Join Cardinality 추정 오류로 인해 비효율적인 실행 계획이 생성되는 문제가 발생하였다.  
특히 다음과 같은 경우에서 문제가 두드러졌다.

- PK-FK Join
- OR 조건이 포함된 Join Filter
- 복잡한 Join 조건이 포함된 쿼리

이러한 문제는 Optimizer의 Cardinality 추정 오류로 이어져 비효율적인 실행 계획을 유발하였다.

---

## Problem

- PK-FK 관계에서 Join Selectivity 계산이 부정확함
- Join Filter에 OR 조건이 포함될 경우 비효율적인 실행 계획 생성
- 그 결과 불필요한 Full Scan 발생
- 전체 쿼리 실행 시간이 크게 증가

---

## Implementation

### 1️⃣ PK-FK Join Selectivity 개선

- Primary Key / Foreign Key 관계에 대한 Join Selectivity 계산 로직 재설계
- Cardinality 추정 정확도 향상
- Join Order 결정을 위한 Cost Model 입력값 개선

---

### 2️⃣ OR 조건 Join Filter 최적화

- Join Filter에 OR 조건이 포함된 경우 최적 실행 계획을 생성할 수 있도록 Optimizer 로직 개선
- Predicate Selectivity 계산 로직 개선
- Plan Branching 및 Cost 비교 로직 개선

---

## Outcome

### PK-FK Join Query Execution Time

```
5s → 1s
```

### OR-Condition Join Query Execution Time

```
3s → 0.8s
```

### Table Partition Pruning 성능 개선

```
827.13 ms → 27.24 ms
```

결과적으로 RDBMS 엔진 내에서 **Join 실행 계획의 품질이 크게 향상되었으며 Optimizer 의사결정 안정성이 개선되었다.**
