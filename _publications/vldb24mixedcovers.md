---
title: "Mixed Covers of Keys and Functional Dependencies for Maintaining the Integrity of Data under Updates (CCF-A)"
collection: publications
category: conferences
permalink: 
excerpt: ''
date: 2024-03-01
venue: 'VLDB'
paperurl: 'https://www.vldb.org/pvldb/vol17/p1578-link.pdf'
citation: '<strong>Zhuoxing Zhang</strong>, and Sebastian Link. "Mixed covers of keys and functional dependencies for maintaining the integrity of data under updates." Proceedings of the VLDB Endowment 17, no. 7 (2024): 1578-1590.'
---

Covers for a set of functional dependencies (FDs) are fundamental for many areas of data management, such as integrity maintenance, query optimization, database design, and data cleaning. When declaring integrity constraints, keys enjoy native support in database systems while FDs need to be enforced by triggers or at application level. Consequently, maximizing the use of keys will provide the best support. We propose the new notion of mixed cover for a set of FDs, comprising the set of minimal keys together with a cover for the set of non-key FDs implied by the FD set. We establish sequential and parallel algorithms for computing mixed covers from a given set of FDs, and illustrate that they complement each other in terms of their performance. Even though FD covers are typically smaller in number or size than their corresponding mixed cover, the latter generate orders of magnitude lower overheads during integrity maintenance. We also quantify how mixed covers improve the performance of query, refresh and insert operations on the TPC-H benchmark under different constraint workloads.
