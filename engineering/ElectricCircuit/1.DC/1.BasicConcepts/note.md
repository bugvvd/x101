# Basic Concepts

An electric circuit is an interconnection of electrical elements.

```latex {cmd=true hide}
\documentclass{standalone}
\usepackage[siunitx]{circuitikz}
\begin{document}
  \begin{circuitikz}[scale=2]
    \draw (0,0) to[isource] (0,1) -- (1,1) to[R] (1,0) -- (0,0);
  \end{circuitikz}
\end{document}
```

1.2 SI

1.3 Charge and Current

**Charge** Charge is an electrical property of the atomic particles of which matter consists, measured in coulombs $C$.

the charge $e$ on an electron is negative

$$
e = -1.602 \times 10^{-19} C.
$$

**Electric current** is the time rate of change of charge, measured in amperes $A$.

$$
1 \,A = 1 \, C/\sec
$$

$$
\begin{align*}
i &\triangleq \frac{dq}{dt}\\
Q &\triangleq \int_{t_0}^{t} i \, dt\\
\end{align*}
$$


$$
$$

