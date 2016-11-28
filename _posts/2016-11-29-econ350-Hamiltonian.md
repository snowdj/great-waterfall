---
published: false
layout: post
title: Hamiltonian and Stock-Flow Problem
category: econ350
tags:
  - Hamiltonian
  - Dynamic programming
  - Bellman equation
---
### 45 Stock-Flow problem

Lagrangean

factor out y_t in Lagrangean

take derivative with respect to y_t


$$
\pi_{t+1} -\pi_{t} = -[F_{Y_t} + \pi_{t+1} Q_{Y_t}  ]
$$

where $Y_{t+1} - Y_{t} = Q_{t}$.



#### Hamiltonian

$$
H(Y_t, Z_t, \pi_{t+1}, t) = F(Y_t, Z_t,t) +  \pi_{t+1} Q(Y_t, Z_t, \pi_{t+1}, t)
$$

Or

$$
\pi_{t+1} -\pi_{t} = -H_{Y_{t}}
$$

For each period , maximize H by choosing Z_t Y_t in peroid t.


### 47 Maximum principle

2. maximum principle

Transform dynamic problem into a equence of static problems that are connectec by inter temporal euqations.



3. Intertemporal connector for $\pi$.

