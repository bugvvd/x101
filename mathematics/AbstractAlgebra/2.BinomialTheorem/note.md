# 2. Number Theory

## 2.1. Binomial Theorem

The expansion of $(1 + x)^{n}$ is an expression of the form,

$$
c_{0} + c_{1}x + c_{2}x + \cdots + c_{n - 1}x^{n - 1} + c_{n}x^{n}   
$$

The coefficients $c_{k}$ are called **binomial coefficients**.

In elementary algebra, the binomial theorem (or binomial expansion) describes the algebraic expansion of powers of a binomial.

We denote coefficient $c_{k} = \tbinom{n}{k}$ as "$n$ chose $k$" because there is a combinitorical interpretation for it.

If we write $(1 + x)^{n}$ as a product,

$$
\begin{matrix}
\underbrace{(1 + x)(1 + x) \cdots (1 + x)} \\ n
\end{matrix}
$$

then accoding to the **distributive law** there will be one term for each choice of either $1$ or $x$ from each of the binomails $(1 + x)$ of the product.

When it comes to, for example, term $x^{k}$ which is essentially $1^{n-k}x^{k}$, we have in total $c_{k}$ **like terms** adds together, one for each way of choosing exactly $k$ from $n$ binomials to contribute a $x$. Therefore from a conbinitorics point of view, $c_{k}$ is the ways of choosing exactly $k$ elements from a $n$-elements set. 

The expansion is thus written,

$$
(1 + x)^{n} = \sum_{k = 0}^{n}\dbinom{n}{k}x^{k}
$$

By observing the values and their positions in **Pascal Triangle** we can roughly conclude that,

$$
\dbinom{n}{k} = \dbinom{n - 1}{k - 1} + \dbinom{n - 1}{k}
$$

We can prove the it.

**Lemma 2.1**

For integers $n \ge 1$ and all $k$ with $1 \le k \le n$，

$$
\dbinom{n + 1}{k} = \dbinom{n}{k - 1} + \dbinom{n}{k}
$$

**Proof**


