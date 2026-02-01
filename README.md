# Overview

Database Engineer with experience in **RDBMS core engineering**(![Tibero](https://img.shields.io/badge/Tibero-TIBERO-red)), SQL optimization, and query optimizer development** at an enterprise database vendor.

- Developed internal **SQL Tuning Advisor** and **SQL Plan Management (SPM)** features
- Improved query performance through **cost-based optimization and statistics accuracy**
- Resolved production performance regressions in enterprise and financial systems
- Achieved measurable latency reductions from seconds to milliseconds

**Core Skills**  
RDBMS Internals · SQL / PL/SQL · Cost-Based Optimization · Execution Plans · Statistics · C

> Source code is not public due to company policy.  
> This repository documents system design, internal logic, and performance impact.
---
# Case Studies
- [![SQL Plan Management](https://img.shields.io/badge/Docs-SQL%20Plan%20Management-2ea44f?style=for-the-badge)](./sql-plan-management.md)
- [![SQL Tuning Advisor](https://img.shields.io/badge/Docs-SQL%20Tuning%20Advisor-0969da?style=for-the-badge)](./sql-tuning-advisor.md)
- [![Index Statistics Improvement](https://img.shields.io/badge/Docs-Index%20Statistics%20Improvement-0969da?style=for-the-badge)](./index-statistics-improvement.md)
---
# Architecture
- [![Index Statistics Improvement](https://img.shields.io/badge/Docs-Architecture-0969da?style=for-the-badge)](./architecture-overview.md)
---
# Production Issue Resolution for Enterprise RDBMS Clients

## Context
Enterprise customers using the in-house RDBMS experienced critical issues during production operations, including performance degradation, database downtime, and unstable query behavior.

## Issues Encountered
- Severe query performance degradation under real workloads
- Database downtime incidents requiring urgent analysis
- Optimizer misbehavior caused by missing, stale, or skewed statistics

## Approach
- Analyzed customer workloads, execution plans, and statistics
- Identified root causes at the optimizer, statistics, and execution engine levels
- Applied targeted fixes and tuning without impacting query correctness
- Validated solutions through reproducible test cases and customer verification

## Outcome
- Restored stable database operations for enterprise and financial clients
- Prevented recurrence through improved statistics handling and optimizer behavior
- Increased customer confidence in database reliability and performance
