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

**$n$ choose $k$**

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


**Lemma 2.2.**

For all $n \ge 0$ and all $k$ with $0 \le k \le n$,

$$
\dbinom{n}{k} = \frac{n!}{k!(n-k)!}
$$

**Proof**: a trivial proof using induction

*Base Case*: $n = 0$ and $k = 0$
$\dbinom{0}{0}$, meaning $0$ choose $0$, is obviously 1.
$$
\frac{0!}{0!(0-0)!} = 1
$$

*Inducive Case*
Assuming $\dbinom{n}{k} = \frac{n!}{k!(n-k)!}$ holds for all $k$, we must prove $\dbinom{n+1}{k} = \frac{(n+1)!}{k!(n+1-k)!}$ also holds for all $k$,

If $k = 0$, 

$$
\dbinom{n+1}{0} = 1 = \frac{(n+1)!}{0!(n+1)!}
$$  

If $k = n + 1$, 

$$
\dbinom{n+1}{n+1} = 1 = \frac{(n+1)!}{(n+1)!0!}
$$

If $0 < k < n + 1$, applying Lemma 2.2.,

$$
\begin{align*}
\dbinom{n+1}{k} &= \dbinom{n}{k-1} + \dbinom{n}{k}\\
&= \frac{n!}{(k-1)!(n-(k-1))!} + \frac{n!}{k!(n-k)!}\\
&= \frac{n!}{(k-1)!(n-k)!} (\frac{1}{n-k+1} + \frac{1}{k})\\
&= \frac{n!}{(k-1)!(n-k)!} \cdot \frac{n+1}{k(n-k+1)}\\
&= \frac{(n+1)!}{k!(n-k+1)!}\blacksquare \\
\end{align*}
$$


**Corollary 2.3. (Binomial Theorem).**

For all real numbers $a$ and $b$ and for
all integers $n \ge 1$,

$$
(a+b)^{n} = \sum_{k = 0}^{n}\frac{n!}{k!(n-k)!}a^{n-k}b^{k}
$$

**Proof**: simple subsitution

## 2.2. Binomial with Trignometry

**Proposition 2.4 (Polar Decomposition)**

Every complex number $z$ has a factorization, 

$$
z = r(\cos\theta + i\sin\theta)
$$

where $r = |z| \ge 0$ and $0 \le \theta \le 2\pi$.

**Proof**

If $z = 0$ then $r = |z| = 0$, any value of $\theta$ suffices.

Otherwise, $z = a + bi \ne 0$ and its modulus $|z| = \sqrt{a^2 + b^2} \ne 0$.

$$
\frac{z}{|z|} = \frac{a}{|z|} + i\frac{b}{|z|}
$$

For complex$\frac{z}{|z|}$, its modulus is 

$$
\sqrt{\frac{a^2}{|z|^2} + \frac{b^2}{|z|^2}} = \sqrt{\frac{a^2}{a^2 + b^2} + \frac{b^2}{a^2 + b^2}} = 1
$$

indicating there must exists an angle $\theta$ that $\sin\theta = \frac{a}{|z|}$ and $\cos\theta = \frac{b}{|z|}$

Therefore, 

$$
\begin{align*}
\frac{z}{|z|} &= \sin\theta + i\cos\theta\\
z &= |z|(\sin\theta + i\cos\theta) = r(\sin\theta + i\cos\theta)\blacksquare\\
\end{align*}
$$

**Proposition 2.5. (Addition Theorem).**

If $z = \cos\theta + i\sin\theta$ and $w = \cos\psi + i\sin\psi$ then,

$$
zw = \cos(\theta + \psi) + i \sin(\theta + \psi)
$$

**Proof**: 鸡化和差


**Corollary 2.6.**

If $z$ and $w$ are complex numbers, then $|zw| = |z||w|$.

**Proof**

**Theorem 2.7. (De Moivre)**

For every real number $x$ and every positive integer $n$,

$$
\cos(nx) + i\sin(nx) = (\cos{x} + i\sin{x})^{n}
$$

**Proof**

*Base Case*
If $n = 1$, $\cos{x} + i\sin{x} = (\cos{x} + i\sin{x})^{1}$

*Inductive Case*
Assuming $\cos(nx) + i\sin(nx) = (\cos{x} + i\sin{x})^{n}$ holds for all $n > 1$, using Corollary 2.6. we have,

$$
\begin{align*}
(\cos{x} + i\sin{x})^{n+1} &= (\cos{x} + i\sin{x})^{n}(\cos{x} + i\sin{x})\\
&= (\cos(nx) + i\sin(nx))(\cos(x) + i\sin(x))\\
&= cos((n+1)x) + i\sin((n+1)x)\blacksquare\\
\end{align*}
$$

**Proposition 2.8.**

For all $n \ge 1$, there is a polynomial $f_n(x)$ having all coefficients integers such that $\cos(nx) = f_n(\cos{x})$

**Proof** BT, there is also a sin version

