# Case Study: SQL Plan Management (SPM)

## Context

통계 정보 변경이나 시스템 업그레이드 이후  
**실행 계획(Execution Plan)의 불안정성**으로 인해 성능 저하가 발생하는 문제가 있었다.

## Problem

- Optimizer가 실행 계획을 변경하면서 기존에 안정적으로 동작하던 워크로드의 성능이 저하될 수 있음
- 검증된 실행 계획을 강제로 유지할 수 있는 신뢰성 있는 메커니즘이 존재하지 않았음

## Implementation

다음과 같은 **SQL Plan Management (SPM)** 기능을 구현하였다.

- `OPTIMIZER_USE_SQL_PLAN_BASELINES`
- `EVOLVE_SQL_PLAN_BASELINE`

주요 구현 내용:

- 저장된 **Plan Baseline 중 최저 Cost 계획을 선택하도록 Optimizer 동작 개선**
- 기존에 비활성화된 Plan을 **안전하게 검증하고 활성화할 수 있는 Evolution 기능 구현**

## Outcome

- 실행 계획 안정성 향상
- 쿼리 성능 예측 가능성 개선
- 해당 기능은 **엔터프라이즈 RDBMS 제품 기능으로 릴리스**
