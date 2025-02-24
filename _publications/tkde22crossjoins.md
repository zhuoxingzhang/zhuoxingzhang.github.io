---
title: "Discovery of Cross Joins (CCF-A)"
collection: publications
category: manuscripts
permalink: 
excerpt: ''
date: 2022-07-21
venue: 'TKDE'
slidesurl: ''
paperurl: 'https://ieeexplore.ieee.org/abstract/document/9835144'
citation: 'Miika Hannula, <strong>Zhuoxing Zhang</strong>, Bor-Kuan Song, and Sebastian Link. "Discovery of cross joins." IEEE Transactions on Knowledge and Data Engineering 35, no. 7 (2022): 6839-6851.'
---

A cross join between two attribute sets holds on a relation whenever its projection onto the union of the attribute sets is the cross join between its projections on the first and second attribute set. Hence, the cross join is a fundamental operator on database relations. For example, it can rewrite the division operator into a simple projection, or measure the independence of tuple values between two attribute sets during cardinality estimation. It is therefore surprising that we present the first research on the discovery problem of cross joins. We show that the problem of deciding whether there is a cross join that holds on a given relation is not only NP-complete but W[3]-complete in its arguably most natural parameter, namely its arity. We establish the first algorithms that discover all cross joins that hold on a given relation. We illustrate in experiments with benchmark data that our algorithms perform well within the limits established by our hardness results. Our treatment of cross joins and the design of our algorithms enables us to extend our findings to the discovery of cross joins that meet a given approximation ratio. Our experiments quantify the trade-off between discovery time and targeted ratio.
