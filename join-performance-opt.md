# Case Study: Join Performance Optimization

## Context  
Join cardinality misestimation caused inefficient execution plans, particularly in PK-FK joins and complex OR-filtered join conditions.

## Problem  
- Inaccurate join selectivity calculation for PK-FK relationships  
- Suboptimal plan generation when OR conditions were present in join filters  
- Resulting in unnecessary full scans and high execution time  

## Implementation  

1️⃣ PK-FK Join Selectivity Enhancement  
- Redesigned join selectivity calculation logic for primary-key / foreign-key relationships  
- Improved cardinality estimation accuracy  
- Refined cost model input for join order decision  

2️⃣ OR-Condition Join Filter Optimization  
- Implemented optimizer logic to generate optimal plans when join filters contain OR conditions  
- Enhanced predicate selectivity handling  
- Improved plan branching and cost comparison logic  

## Outcome  

- PK-FK Join Query Execution Time:  
  5s → 1s  

- OR-Condition Join Query Execution Time:  
  3s → 0.8s  

- Targeted feature segment improvement:  
  827.13 ms → 27.24 ms  

Resulted in significantly improved join plan quality and optimizer decision stability within the RDBMS engine.
