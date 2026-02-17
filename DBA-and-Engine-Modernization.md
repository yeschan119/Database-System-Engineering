# Case Study: Production DB Performance Engineering & Engine Modernization

## Context  
As part of the Optimizer Team, I handled production database issues from enterprise customers (average 2+ cases per week).  
Most issues were performance-related, requiring deep understanding of query plans, statistics, and database internals.

In parallel, I participated in modernizing legacy engine components written in C by migrating them to C++.

---

## Problem  

1️⃣ Customer Production Performance Issues  
- Query performance degradation in production environments  
- Suboptimal execution plans due to statistics, schema design, or architecture limitations  
- Some issues not solvable through SQL tuning alone  

2️⃣ Legacy Code Maintainability  
- Core engine modules written in legacy C  
- Limited modularity and maintainability  
- Increasing difficulty in extending optimizer-related logic  

---

## Implementation  

### 🔹 Customer DB Performance Resolution  

1. Query Tuning  
   - Analyzed execution plans and cardinality estimation  
   - Adjusted statistics and index strategies  
   - Rewrote complex queries when necessary  

2. Database Architecture Redesign  
   - Proposed schema restructuring  
   - Index strategy redesign  
   - Partitioning strategy optimization  
   - Improved workload distribution  

3. Engine-Level Patch Development  
   - When tuning was insufficient, implemented engine patches  
   - Modified optimizer logic or statistics behavior  
   - Delivered patched binaries to resolve root causes  

---

### 🔹 Legacy Engine Migration (C → C++)  

- Refactored legacy C modules into modern C++  
- Improved modular structure and code maintainability  
- Applied object-oriented design principles  
- Enhanced memory safety and readability  
- Prepared engine components for future extensibility  

---

## Outcome  

- Resolved high-impact production performance issues across multiple enterprise customers  
- Reduced average query execution time in critical cases  
- Strengthened optimizer stability under real-world workloads  
- Improved maintainability and extensibility of core engine components  
- Demonstrated ability to operate across DBA-level troubleshooting and engine-level development  

Resulted in increased system reliability and improved customer satisfaction for enterprise RDBMS deployments.
