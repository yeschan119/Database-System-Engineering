# Overview

엔터프라이즈 데이터베이스 벤더에서 **RDBMS 코어 엔지니어링** 경험을 가진 Database Engineer  
[![Tibero](https://img.shields.io/badge/RDBMS-Tibero-red)](https://docs.tibero.com/tibero/en/getting-started/introduction/introduction-guide/introduction-to-tibero)

[English 🇬🇧](README.en.md)

SQL 최적화 및 Query Optimizer 개발을 수행하였다.

- 내부 **SQL Tuning Advisor** 및 **SQL Plan Management (SPM)** 기능 개발
- **Cost-Based Optimization 및 통계 정확도 개선**을 통한 쿼리 성능 향상
- 엔터프라이즈 및 금융 시스템 환경에서 발생한 **운영 성능 저하 문제 해결**
- 초 단위 응답 시간을 **밀리초 단위로 단축**하는 성능 개선 달성

### Core Skills

RDBMS Internals · SQL / PL/SQL · Cost-Based Optimization · Execution Plans · Statistics · C

> 회사 정책에 따라 실제 소스 코드는 공개할 수 없습니다.  
> 본 저장소에는 시스템 설계, 내부 로직, 성능 개선 효과를 문서 형태로 정리하였습니다.

---

# Case Studies

- [![SQL Plan Management](https://img.shields.io/badge/Docs-SQL%20Plan%20Management-2ea44f?style=for-the-badge)](./sql-plan-management.ko.md)
- [![Join Performance Optimization](https://img.shields.io/badge/Docs-Join%20Performance%20Optimization-0969da?style=for-the-badge)](./join-performance-opt.ko.md)
- [![DB Administration & Engine Modernization](https://img.shields.io/badge/Docs-DB%20Administration%20And%20Engine%20Modernization-0969da?style=for-the-badge)](./DBA-and-Engine-Modernization.ko.md)

---

# Architecture

- [![Index Statistics Improvement](https://img.shields.io/badge/Docs-Architecture-0969da?style=for-the-badge)](./architecture-overview.md)

---

# 엔터프라이즈 RDBMS 고객사 운영 이슈 해결

## Context

사내 RDBMS를 사용하는 엔터프라이즈 고객사에서 운영 중 다음과 같은 주요 문제가 발생하였다.

- 쿼리 성능 저하
- 데이터베이스 다운타임
- 불안정한 실행 계획으로 인한 쿼리 동작 문제

---

## Issues Encountered

- 실제 워크로드 환경에서 심각한 쿼리 성능 저하 발생
- 긴급 대응이 필요한 데이터베이스 장애 발생
- 누락되거나 오래된 통계, 혹은 데이터 분포 불균형으로 인한 **Optimizer 오동작**

---

## Approach

- 고객사의 실제 워크로드, 실행 계획, 통계 정보를 분석
- Optimizer, 통계 모듈, 실행 엔진 수준에서 근본 원인 파악
- 쿼리 정확성에 영향을 주지 않도록 **정밀한 튜닝 및 수정 적용**
- 재현 가능한 테스트 케이스와 고객 환경 검증을 통해 해결책 검증

---

## Outcome

- 엔터프라이즈 및 금융 고객사의 **DB 운영 안정성 복구**
- 통계 처리 및 Optimizer 동작 개선을 통해 문제 재발 방지
- 데이터베이스 성능과 안정성에 대한 고객 신뢰도 향상
