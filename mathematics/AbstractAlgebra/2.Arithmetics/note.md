# 2. Arithmetics

## Basic sets

$\mathbb{Q}$: the set of all rational numbers (or fractions), that is, all numbers of the form $a/b$, where $a$ and $b$ are integers and $b \ne 0$ (after the word quotient)

$\mathbb{R}$:  the set of all real numbers

$\mathbb{C}$: the set of all complex numbers

## Division

**Theorem 2.1 (Division Algorithm).**

Given integers $a$ and $b$ with $a \ne 0$, there exist unique integers $q$ and $r$ with,

$$
b = qa + r, 0 \le r \le |a|
$$

**Proof**: WOP, Least Integer Axiom, only in $a > 0 \& b \ge 0$, uniqueness of $q \& r$

**Definition.** If $a$ and $b$ are integers with $a \ne 0$, then the integers $q$ and $r$ occurring in the division algorithm are called the **quotient** and the **remainder** after dividing $b$ by $a$.

**Corollary 2.2.**

There are infinitely many primes

**Proof**

**Definition**. If $a$ and $b$ are integers, then $a$ is a divisor of $b$ if there is an integer $d$ with $b = ad$(synonyms are $a$ divides $b$ and also $b$ is a multiple of $a$). We denote this by $a \mid b$




## Factorization


**Definition.** A common divisor of integers $a$ and $b$ is an integer $c$ with $c \mid a$ and $c \mid b$. The greatest common divisor of $a$ and $b$, denoted by $\gcd(a, b)$ is defined by

$$
\gcd(a,b) = 
\begin{cases}
0 \text{ if } a = b = 0 \\
\text{the largest common divisor of } a \text{ and } b \text{ otherwise}
\end{cases}
$$

**Definition.** A linear combination of integers $a$ and $b$ is an integer of the form $sa + tb$ where $s$ and $t$ are integers.

**Theorem 2.3.**

If $a$ and $b$ are integers, then $\gcd(a, b)$ is a linear combination of $a$ and $b$.

**Proof**: Least Integer Axiom

**Corollary 2.4.**

Let $I$ be a subset of $\mathbb{Z}$ such that

1. $0$ is in $I$
2. if $a$ and $b$ are in $I$ , then $a - b$ is in $I$
3. if $a$ is in $I$ and $q$ is in $\mathbb{Z}$ , then $qa$ is in $I$

Then there is a nonnegative integer $d$ in $I$ with $I$ consisting precisely of all the
multiples of $d$.

**Proof**: Least Integer Axiom


**Theorem 2.5. (Euclid's Lemma)**

**Theorem 2.6. (Euclidean Algorithm)**


## Equivalence Relations

## Congruences
