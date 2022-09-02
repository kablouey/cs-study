---
tags:
  - alg
---
# Euclid's Algorithm
## Problem
Find $GCD(m,n)$ of two non-negative integers $m$ and $n$.
eg. $GCD(60,24)=12$

## Solution
Euclid's is based on repeated application of the equality $GCD(m,n) = GCD(n, m\,mod\,n)$ until $n=0$ giving result $m$
eg. $GCD(60,24) = GCD(24,12) = GCD(12,0)$

## Pseudocode
```
ALGORITHM Euclid(m,n)
// Computes GCD(m,n) by Euclid's algorithm
// INPUT: Two non-negative integers m and n
// OUTPUT: Greatest Common Divisor of m and n
  1. if n > 0 then
  2.   return GCD(n, m mod n)
  3. end if
  4. return m
```
## Alternative - Common primes
1. Find the prime factors of $m$
2. Find the prime factors of $n$
3. Identify all common factors in the two prime expansions
4. Compute the product of all common factors and return it as the $GCD(m,n)$
eg. 
$$
\begin{aligned}
60=2\cdot2\cdot3\cdot5 \\
24=2\cdot2\cdot3 \\
GCD(60,24)=2\cdot2\cdot3=12
\end{aligned}
$$