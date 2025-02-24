---
title: "Substructure-aware Log Anomaly Detection (CCF-A)"
collection: publications
category: conferences
permalink: 
excerpt: ''
date: 2025-02-20
venue: 'VLDB'
paperurl: 'https://www.vldb.org/pvldb/vol18/p213-tang.pdf'
citation: 'Yanni Tang, <strong>Zhuoxing Zhang</strong>, Kaiqi Zhao, Lanting Fang, Zhenhua Li, and Wu Chen. "Substructure-aware log anomaly detection." Proceedings of the VLDB Endowment 18, no. 2 (2024): 213-225.'
---

System logs, recording critical information about system operations, serve as indispensable tools for system anomaly detection. Graph-based methods have demonstrated superior performance compared to other methods in capturing the interdependencies of log events. However, existing methods often neglect the complex substructure patterns of nodes within log graphs, making it challenging to capture the subtle alteration in event type, structure, and the location of exceptions that indicate node anomalies. To address this limitation, this paper proposes a novel framework called Substructure-aware Log Anomaly Detection at Code File Level (SLAD). It first introduces a Monte Carlo Tree Search strategy tailored specifically for log anomaly detection to discover representative substructures. Then, SLAD incorporates a substructure distillation way to enhance the efficiency of anomaly inference based on the representative substructures. After that, we introduce a soft pruning to obtain key substructure for nodes. Experimental results show SLAD outperforms all baselines. Particularly, SLAD demonstrates at least 15 times faster than substructure-based graph learning methods in anomaly inference.
