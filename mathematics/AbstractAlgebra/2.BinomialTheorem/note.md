# 2. Number Theory

## 2.1. Binomial Theorem

The expansion of $(1+x)^{n}$ is an expression of the form,

$$
c_{0}+c_{1}x+c_{2}x+\cdots+c_{n-1}x^{n-1}+c_{n}x^{n}   
$$

The coefficients $c_{k}$ are called **binomial coefficients**.

In elementary algebra, the binomial theorem (or binomial expansion) describes the algebraic expansion of powers of a binomial.

We denote coefficient $c_{k} = \tbinom{n}{k}$ as "$n$ chose $k$" because there is a combinitorical interpretation for it.

**Combinatorial Interpretation for Binomial Coefficient**

If we write $(1+x)^{n}$ as a product,

$$
\begin{matrix}
\underbrace{(1+x)(1+x) \cdots (1+x)} \\ n
\end{matrix}
$$


then accoding to the **distributive law** there will be one term for each choice of either $1$ or $x$ from each of the binomails $(1+x)$ of the product.

When it comes to, for example, term $x^{k}$ which is essentially $1^{n-k}x^{k}$, we have in total $c_{k}$ **like terms** adds together, one for each way of choosing exactly $k$ from $n$ binomials to contribute a $x$. Therefore from a conbinitorics point of view, $c_{k}$ is the ways of choosing exactly $k$ elements from a $n$-elements set. 

The expansion is thus written,

$$
(1+x)^{n} = \sum_{k = 0}^{n}\dbinom{n}{k}x^{k}
$$

**$n$ choose $r$**

[link to combinitorical explanation](goto)

Binomial coefficients have some good properties. By observing the values and their positions in **Pascal Triangle** we can roughly conclude that,

$$
\dbinom{n}{k} = \dbinom{n-1}{k-1}+\dbinom{n-1}{k}
$$

We can prove the it.

**Lemma 2.1. (Pascal's rule)**

For integers $n \ge 1$ and all $k$ with $1 \le k \le n$，

$$
\dbinom{n+1}{k} = \dbinom{n}{k-1}+\dbinom{n}{k}
$$

**Proof**

For all $n \ge 1$,

$$
(1+x)^{n} = c_{0} + c_{1}x + c_{2}x^{2} + \cdots + c_{n-1}x^{n-1} + c_{n}x^{n}
$$

Coefficient $c_{k}$ for $x^{k}$ is $\dbinom{n}{k}$ and $\dbinom{n+1}{k}$ is the coefficient for $x^{k}$ in $(1+x)^{n+1}$.

Expanding $(1+x)^{n+1}$ we have, 
$$
\begin{align*}
(1+x)^{n+1} &= (1+x)(1+x)^{n}\\
&=(1+x)c_{0} + (1+x)c_{1}x + (1+x)c_{2}x^{2} + \cdots + (1+x)c_{n-1}x^{n-1} + (1+x)c_{n}x^{n}\\
&= (c_{0} + c_{1}x + c_{2}x^{2} + \cdots + c_{n-1}x^{n-1} + c_{n}x^{n}) + x(c_{0} + c_{1}x + c_{2}x^{2} + \cdots + c_{n-1}x^{n-1} + c_{n}x^{n})\\
&= c_{0} + (c_{0} + c_{1})x + (c_{1} + c_{2})x^{2} + \cdots + (c_{n-2} + c_{n-1})x^{n-1} +(c_{n-1} + c_{n})x^{n} + c_{n}x^{n+1}
\end{align*}
$$

According to the expansion, for $1 \le k \le n$, we can see the coefficient for $x^{k}$ is $c_{k-1} + c_{k}$, which are $\dbinom{n}{k-1}$ and $\dbinom{n}{k}$ respectively.

Thus $\dbinom{n+1}{k}$, the coefficient for $x^{k}$in $(1+x)^{n+1}$ suffices,

$$
\dbinom{n+1}{k} = \dbinom{n}{k-1}+\dbinom{n}{k}
\blacksquare
$$


**Proposition 2.2.**

For all $n \ge 0$ and all $k$ with $0 \le k \le n$,

$$
\dbinom{n}{r} = \frac{n!}{r!(n-r)!}
$$

**Proof**: a trivial proof using induction

**Corollary 1.17 (Binomial Theorem).**

For all real numbers $a$ and $b$ and for
all integers $n \ge 1$,

$$
(a+b)^{n} = \sum_{k = 0}^{n}(\frac{n!}{k!(n-k)!})a^{n-k}b^{k}
$$

**Proof**: simple subsitution