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
\cos{nx} + i\sin{nx} = (\cos{x} + i\sin{x})^{n}
$$

**Proof**

*Base Case*
If $n = 1$, $\cos{x} + i\sin{x} = (\cos{x} + i\sin{x})^{1}$

*Inductive Case*
Assuming $\cos{nx} + i\sin{nx} = (\cos{x} + i\sin{x})^{n}$ holds for all $n > 1$, using Corollary 2.6. we have,

$$
\begin{align*}
(\cos{x} + i\sin{x})^{n+1} &= (\cos{x} + i\sin{x})^{n}(\cos{x} + i\sin{x})\\
&= (\cos{nx} + i\sin{nx})(\cos{x} + i\sin{x})\\
&= \cos{(n+1)x} + i\sin{(n+1)x}\blacksquare\\
\end{align*}
$$

**Proposition 2.8.**

For all $n \ge 1$, there is a polynomial $f_n(x)$ having all coefficients integers such that,

$$
\cos{nx} = f_n(\cos{x})\\
\sin{nx} = g_n(\sin{x})
$$

**Proof** BT, there is also a sin version

By Theorem 2.7.,

$$
\begin{align*}
\cos{nx} + i\sin{nx} &= (\cos{x} + i\sin{x})^{n}\\
&= \sum_{k=0}^{n}\dbinom{n}{k}\cos^{n-k}{x}(i\sin{x})^k\\
\end{align*} 
$$

For the equation to hold, the real part of the left side must equal that of the right side.

$$
\begin{align*}
\cos{nx} &= \sum_{k \text{ is even}}^{n}\dbinom{n}{k}(\cos{x})^{n-k}(i\sin{x})^k\\
&= \sum_{p=0, p \in \mathbb{Z}^{+}}^{\lfloor n/2 \rfloor}\dbinom{n}{2p}\cos^{n-2p}{x} \cdot i^{2p} \cdot \sin^{2p}{x}\\
&= \sum_{p=0, p \in \mathbb{Z}^{+}}^{\lfloor n/2 \rfloor}(-1)^{p}\dbinom{n}{2p}\cos^{n-2p}{x}(1-\cos^2{x})^{p}\\
\end{align*}
$$

Also for the complex part,

$$
\begin{align*}
i\sin{nx} &= \sum_{k \text{ is odd}}^{n}\dbinom{n}{k}\cos^{n-k}{x}(i\sin{x})^k \\
&= i\sum_{q=0, q \in \mathbb{Z}}^{\lfloor (n-1)/2 \rfloor}\dbinom{n}{2q+1}(\cos{x})^{n-(2q+1)}\sin^{2q+1}{x}\\
&= i\sum_{q=0, q \in \mathbb{Z}}^{\lfloor (n-1)/2 \rfloor}\dbinom{n}{2q+1}(1-\sin^2{x})^{\frac{n-1}{2} + q}\sin^{2q+1}{x}\\
\sin{nx} &= \sum_{q=0, q \in \mathbb{Z}}^{\lfloor (n-1)/2 \rfloor}\dbinom{n}{2q+1}(1-\sin^2{x})^{\frac{n-1}{2} - q}\sin^{2q+1}{x} \blacksquare\\
\end{align*} 
$$

**Theorem 2.9. (Euler's Theorem)**

For all real numbers $x$,

$$
e^{ix} = \cos{x}+i\sin{x}
$$

**Proof**

The Maclaurin series of $f(x)=e^{ix}$ is,

$$
\begin{align*}
e^{ix}&=\sum_{n=0}^{\inf}\frac{f^{(n)}(0)}{n!}(x-0)^{n}\\
&=1+\frac{i}{1!}x+\frac{i^2}{2!}x^2+\cdots+\frac{i^n}{n!}x^{n}+\cdots\\
&=1+ix-\frac{x^2}{2!}-\frac{ix^3}{3!}+\frac{x^4}{4!}-\frac{ix^5}{5!}+\cdots\\
&=(1-\frac{x^2}{2!}+\frac{x^4}{4!}-\frac{x^6}{6!}+\cdots)+i(x-\frac{x^3}{3!}+\frac{x^5}{5!}-\frac{x^7}{7!}+\cdots)\\
&=\cos{x}+i\sin{x}\blacksquare\\
\end{align*}
$$

Specially when $x = \pi$,

$$
e^{i\pi}=-1
$$

**Definition** If $n \ge 1$ is an integer, then an nth root of unity is a complex number
$\zeta$ with $\zeta^{n} = 1$.

**Corollary 2.10.** Every nth root of unity $\zeta$ is equal to,

$$
e^{2\pi ik/n} = \cos{(2k\pi/n)} + i\sin{(2k\pi/n)}
$$

for some $k$ with $0 \le k \le n-1$.

**Proof**

By Proposition 2.4., there must exist  a factorization for $\zeta$ that 

$$
\zeta = |\zeta|(\cos{\theta}+i\sin{\theta})
$$

By Corollary 2.6., 

$$
|\zeta^{n}|=|\underbrace{\zeta \times \zeta \cdots \times \zeta}_{n}|=\underbrace{|\zeta| \times |\zeta| \times \cdots \times |\zeta|}_{n} = 1
$$

Therefore, $|\zeta| = 1, \zeta = \cos{\theta}+i\sin{\theta}$
By De Moivre's Theorem 2.7., 

$$
\zeta^{n}= (\cos{\theta}+i\sin{\theta})^{n}=\cos{n\theta}+i\sin{n\theta}
$$

This equation holds iff $\cos{n\theta}=1$ and $\sin{n\theta}=0$. Therefore,

$$
\begin{align*}
\theta &= 2k\pi/n\\
\zeta &= \cos{(2k\pi/n)}+i\sin{(2k\pi/n)}=e^{2\pi ik/n}\blacksquare
\end{align*}
$$.

Given $|\zeta|=1$, the all the nth roots of unity lie evenly spaced on the unit circle.