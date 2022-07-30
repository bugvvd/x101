# 1. Recurrent Problems

## 1.1 The Tower of Hanoi
Think of the Tower of Hanoi as a state machine, what we care the most and also the piercing angle is the state of the tower, rather than the process of actual movements.

The state of interest is right before moving the $n^{th}$ plate.

Because we can either conclude from experience or deduce by analysis that to move $n$ plates, 3 steps are necessary. 

- step 1: to be able to move the the $n^{th}$ plate, we must before that move $n-1$ plates to another peg, which takes $T_{n-1}$ steps,
- step 2: to move the $n^{th}$ plate to the destined peg, we need 1 step,
- step 3: to move $n-1$ plates together above the $n^{th}$, which is a mirror operation of step 1, we need another $T_{n-1}$ steps,

In total, to transfer $n$ disks we need,
$$
T_n \le 2T_{n - 1} + 1
$$

The formular uses $ \le $ instead of $ = $ because we only know by now that $ 2T_n + 1 $ suffice.

However the only possible state to move the $n^th$ plate is that $n-1$ plates have already been transfered to another peg, which took $T_{n-1}$ steps. **ONLY for the sake of mathematical sufficiency, one may erroneously moving the $n^th$ plate more than once.** Finally the mirror mirror operation also takes $T_{n-1}$ steps. 
In total, to transfer $n$ disks we need,
$$
T_n \ge 2T_{n - 1} + 1
$$

While I think reaching $T_n = 2T_{n - 1} + 1$ can simply be done by analysing the state of moving the $n^{th}$ plate.

Combining $T_0 = 0$ we have a set of equations, we ourselves have a **recurrence**
$$
\begin{equation*} 
    % \begin{split}
    % \begin{aligned}
    \begin{align}
        &T_0 = 0 \\
        &T_n \ge 2T_{n - 1} + 1 \hspace{10em}
    % \end{split}
    % \end{aligned}
    \end{align}
\end{equation*}
$$

A recurrence is a set of equations that have:
- a boundary value
- an equation for the **general** value in terms of earlier ones

This set of equalities is computationally viable. But a **solution** to this set would greatly simplify the computation.


**Close Form Expression**: A mathematical expression that uses a finite number of standard operations to the arguments. Closed-form expressions are of interest when trying to develop general solutions to problems.



## 1.2 Lines in the plate

