# Basic Concepts

```latex {cmd=true hide}
\documentclass{standalone}
\usepackage[siunitx]{circuitikz}
\begin{document}
  \begin{circuitikz}[scale=2]
    \draw (0,0) to[isource] (0,1) -- (1,1) to[R] (1,0) -- (0,0);
  \end{circuitikz}
\end{document}
```
