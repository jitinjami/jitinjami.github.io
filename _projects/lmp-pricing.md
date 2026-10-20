---
layout: page
title: ML for Electricity Market Pricing
description: Master thesis at USI Lugano. Predicting Locational Marginal Prices in near real time with machine learning instead of solving optimal power flow.
importance: 1
category: past
---

Locational Marginal Prices (LMPs) set the price of electricity at each node of a power grid. Computing them means solving an optimal power flow problem, which is slow at scale.

In my master thesis at the <a href="https://www.ci.inf.usi.ch">Institute of Computing, USI Lugano</a>, supported by a MaRS scholarship from the Hasler Foundation, I studied whether machine learning models can predict LMPs in near real time instead.

### Highlights

- Generated ground-truth data with MATPOWER and MOSEK on PGLib-OPF grids.
- Reached a maximum error of 5% across a range of *n-1* security-criterion cases.

### Outputs

- **Paper**: [AI Driven Near Real-time Locational Marginal Pricing Method: A Feasibility and Robustness Study](https://ieeexplore.ieee.org/document/10407905/), IEEE ISGT Europe 2023.
- **Thesis**: [Feasibility and Robustness of Machine Learning algorithms for calculating Locational Marginal Pricing](https://thesis.bul.sbu.usi.ch/theses/2116-2223Jami/pdf?1680767660/), 2023.
