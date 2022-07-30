# 1. Mathematical Induction

Some preparation works for groups, rings and fields.

The well-ordering principle is a property of the positive integers which is equivalent to the statement of the principle of mathematical induction.


A set is called well-ordered if any nonempty subset has a least element. It is called **Least Integer Axiom** if the set is all natural numbers $\mathbb{N}$, or some **Least [Element] Axiom** in other sets. But unless otherwise noted, I use WOP in terms of a property of the positive integers.


The validity of mathematical induction is largely based on(?) Well Ordering Principle (WOP). 


Contrapositive

Proof by contradiction


## The Principle of Mathematical Induction (PMI)

**PMI Theorems**

Let there be a Let $S(n)$ be a family of statements, one for each natural number $n$. Prove the propersition that $S(n)$ is true for all natural numbers $n$ we can make use of **2 forms of PMIs**.

The propersition can be prooved by **standard/first-form induction** if:  

- step 1 (basic case): $S(0)$ is true, and
- step 2 (inductive case)：$S(k)$ being true implies that $S(k + 1)$ is true.

The propersition can be prooved by **strong/second-form induction** if:  

- step 1 (basic case): $S(0)$ is true, and
- step 2 (inductive case)：$S(k)$ being true for all **predecessors** $k$ of $n$ implies that $S(n)$ is itself true.
    > The predecessors of a natural number $n \ge 1$ are the natural numbers $k$ with $k \lt n$ (0 has no predecessor).

**Proof for standard induction**

Failling either step disproves the propersition.

Denote the a collection $C$ of all the natural numbers $n$ whose statement $S(n)$ is false. To prove the proposition is to prove that $C$ is nonempty.

Supposing $C$ is nonempty, according to WOP, there exists a least natural number $m$. 

Since $S(0)$ is true, it must be the case that $m \ge 1$, which means there exists $m - 1 \ge 0$ and $S(m-1)$. 

Since $m$ is the least element in $C$, $S(m-1)$ must be true. But $S(m-1)$ being true while $S(m)$ being false is in contracdiction with step 2. 

We can therefore conclude that $C$ must be empty and $S(n)$ is true for all natural numbers $n$.


**Proof for strong induction**

Failling either step disproves the propersition.

Denote the a collection $C$ of all the natural numbers $n$ whose statement $S(n)$ is false. To prove the proposition is to prove that $C$ is nonempty.

Supposing $C$ is nonempty, according to WOP, there exists a least natural number $m$. 

Since $S(0)$ is true, it must be the case that $m \ge 1$. For all predecessors $0 \le k \le m$, statements $S(k)$ must be true. 

But one's predecessors statements $S(k)$ being true while its statement being false is in contraction with step 2. 

We can therefore conclude that $C$ must be empty and $S(n)$ is true for all natural numbers $n$.


## Proof of equivalence with WOP

[Quite a hack](https://brilliant.org/wiki/the-well-ordering-principle/)
