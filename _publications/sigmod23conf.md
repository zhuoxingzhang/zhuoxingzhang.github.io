---
title: "Composite Object Normal Forms: Parameterizing Boyce-Codd Normal Form by the Number of Minimal Keys (CCF-A)"
collection: publications
category: conferences
permalink: 
excerpt: ''
date: 2023-05-30
venue: 'SIGMOD'
paperurl: 'https://dl.acm.org/doi/abs/10.1145/3588693'
citation: '<strong>Zhuoxing Zhang</strong>, Wu Chen, and Sebastian Link. "Composite Object Normal Forms: Parameterizing Boyce-Codd Normal Form by the Number of Minimal Keys." Proceedings of the ACM on Management of Data 1, no. 1 (2023): 1-25.'
---

We parameterize schemata in Boyce-Codd Normal Form (BCNF) by the number n of minimal keys they exhibit. We show that n quantifies a trade-off between access variety and update complexity. Indeed, access variety refers to the number of different ways by which every entity over the schema is represented uniquely, while update complexity refers to the number of attribute sets for which uniqueness needs to be preserved during updates. As normalization aims at minimizing the level of effort required to preserve data consistency during updates, we establish an algorithm that returns a lossless, dependency-preserving 3NF decomposition where the subset of output schemata not in BCNF is minimized and redundant BCNF schemata are eliminated from the highest to the lowest n exhibited. In particular, if a lossless, dependency-preserving BCNF decomposition exists, our algorithm returns one where the maximum n across all output schemata is minimized. Experiments with synthetic and real-world data quantify the impact of n on the update and query performance over schemata in BCNF with n minimal keys, and show insight into the efficacy of our algorithm suite.
