---
title: "Synthesizing Third Normal Form Schemata that Minimize Integrity Maintenance and Update Overheads: Parameterizing 3NF by the Numbers of Minimal Keys and Functional Dependencies (CCF-A)"
collection: publications
category: conferences
permalink: 
excerpt: ''
date: 2025-06-18
venue: 'SIGMOD'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3725362'
citation: '<strong>Zhuoxing Zhang</strong>, and Sebastian Link. "Synthesizing Third Normal Form Schemata that Minimize Integrity Maintenance and Update Overheads: Parameterizing 3NF by the Numbers of Minimal Keys and Functional Dependencies." Proceedings of the ACM on Management of Data 3, no. 3 (2025): 1-25.'
---

State-of-the-art relational schema design generates a lossless, dependency-preserving decomposition into Third Normal Form (3NF), that is in Boyce-Codd Normal Form (BCNF) whenever possible. In particular, dependency-preservation ensures that data integrity can be maintained on individual relation schemata without having to join them, but may need to tolerate a priori unbounded levels of data redundancy and integrity faults. As our main contribution we parameterize 3NF schemata by the numbers of minimal keys and functional dependencies they exhibit. Conceptually, these parameters quantify, already at schema design time, the effort necessary to maintain data integrity, and allow us to break ties between 3NF schemata. Computationally, the parameters enable us to optimize normalization into 3NF according to different strategies. Operationally, we show through experiments that our optimizations translate from the logical level into significantly smaller update overheads during integrity maintenance. Hence, our framework provides access to parameters that guide the computation of logical schema designs which reduce operational overheads.
