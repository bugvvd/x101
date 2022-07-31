# 1. Mathematical Induction

Some preparation works for groups, rings and fields.

## Terminology

**Definition**
An explanation of the mathematical meaning of a word.

**Axiom**
A basic assumption about a mathematical situation. (a statement we assume to be true).

**Proposition**
A less important but nonetheless interesting true statement.

**Conjecture**
A statement believed to be true, but for which we have no proof. (a statement that is being proposed to be a true statement).

**Proof**
The explanation of why a statement is true.

**Theorem**
A statement that has been proven to be true.

**Lemma**
A true statement used in proving other true statements (that is, a less important theorem that is helpful in the proof of other results).

**Corollary**
A true statment that is a simple deduction from a theorem or proposition.


## Contrapositive and Proof by Contradiction

The contrapositive of an implication "P implies Q" is the implication "(not Q) implies (not P)."

If an implication is true, then so is its contrapositive; conversely, if the contrapositive is true, then so is the original implication. 

One strategy of proof is to prove the contrapositive of the original implication. Although a statement and its contrapositive are logically equivalent, it is sometimes more convenient to prove the contrapositive. 

This method is also called **indirect proof** or **proof by contradiction**.

## The Well-Ordering Principle (WOP)


**Least Integer Axiom**

A set is called well-ordered if any nonempty subset has a least element. It is called **Least Integer Axiom** if the set is all natural numbers $\mathbb{N}$, or some **Least [Element] Axiom** in other sets. But unless otherwise noted, I use WOP in terms of a property of the positive integers.

**Theorem 1.1.**

Every integer $n \ge 2$ is either a prime or a product of primes.

**Proof**


**Theorem 1.2.**

If $m \ge 2$ is a positive integer which is not divisible by any prime $p$ with $p \le \sqrt{m}$, then $m$ is a prime.

**Proof**



## The Principle of Mathematical Induction (PMI)


The well-ordering principle is a property of the positive integers which is equivalent to the statement of the principle of mathematical induction.

The validity of mathematical induction is largely based on(?) Well Ordering Principle (WOP). 


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


## Proof of PMI's equivalence with WOP

[Quite a hack](https://brilliant.org/wiki/the-well-ordering-principle/)
