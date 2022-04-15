# On "index gymnastics"

Regarding what is sometimes called "index gymnastics"—it's tricky to manipulate sums correctly when there are multiple indices involved. The key to it is to remember that $A_\alpha$ (say) really refers to either $A_1$, or $A_2$, or... $A_M$. The index letters are just stand-ins for the numbers, and they don't retain an identity outside of the sum.


Here's a simple example. Suppose I have a quantity $S = \sum_\alpha A_\alpha$, and I'd like an expression for $S^2$. It might be tempting to write
$$
S^2 = S\times S = \left(\sum_\alpha A_\alpha\right) \times \left(\sum_\alpha A_\alpha\right) = \sum_\alpha A_\alpha^2,
$$
but that's wrong. You can see it by looking at an $M=2$ example:
$$
S^2 = (A_1 + A_2)\times(A_1 + A_2) = A_1^2 + A_2^2 + 2A_1 A_2.
$$

To make sure you never make this kind of mistake, when you are manipulating multiple sums, always use distinct indices for summing, like this (the last two lines illustrate the $M=2$ case):
$$
\begin{align}
S^2 
  &= \left(\sum_\alpha A_\alpha\right) \times \left(\sum_\beta A_\beta\right) \\
  &= \sum_\alpha \sum_\beta A_\alpha A_\beta \\
  &= A_1\times A_1 + A_1\times A_2 + A_2\times A_1 + A_2\times A_2 \\
  &= A_1^2 + A_2^2 + 2A_1A_2.
\end{align}
$$
This forces you to properly account for cross terms.



As a trickier example, if I write
$$
R = \sum_\alpha \sum_\beta A_\alpha A_\beta,
$$
and I'd like to take the derivative of $R$ with respect to an $A$, it's tempting to do this:
$$
\frac{\partial R}{\partial A_\alpha} = \sum_\beta A_\beta.
$$
That is, taking the derivative with respect to $A_\alpha$ just knocks the $A_\alpha$ out of the sum. But this is wrong. To see the error, consider the $M=2$ case, so
$$
R = A_1 A_1 + A_1 A_2 + A_2 A_1 + A_2 A_2.
$$
Taking the derivative WRT $A_1$ (say) gives
$$
\frac{\partial R}{\partial A_1} = 2A_1 + 2A_2.
$$
So the naive calculation we did a few lines ago missed a factor of two! That's because that calculation treated $A_\alpha$ as a unique variable, when really it's a symbol that stands for one of the $M$ different variables $A_1$ to $A_M$, depending on what value *either* $\alpha$ *or* $\beta$ happens to take.

When doing computations like this, the safest thing to do is to make sure every sum is over a unique index, and every derivative is with respect to a unique index. This lets the familiar symbolic manipulations do proper bookkeeping over any sums and derivatives. For example, for the derivative of $R$ with respect to one of the $A$'s, do:
$$
\frac{\partial R}{\partial A_\gamma} = \sum_\alpha \sum_\beta \frac{\partial}{\partial A_\gamma} [A_\alpha A_\beta].
$$
Use the normal "first times derivative of the second plus second times derivative of the first":
$$
= \sum_\alpha \sum_\beta [A_\alpha \delta_{\gamma\beta} + A_\beta \delta_{\gamma\alpha}].
$$
Now remember that a sum over $\alpha$ (say) of something with a $\delta_{\gamma\alpha}$ factor just pulls the $\alpha=\gamma$ term out of the sum (the $\delta$ vanishes otherwise). So we get
$$
= \sum_\alpha A_\alpha + \sum_\beta A_\beta = 2\sum_\alpha A_\alpha.
$$

So introducing that extra index let us get the bookkeeping right. Maybe that helps clear up some of the index gymnastics in some of the BDA lectures (e.g., the Monte Carlo variance calculation in Lec12, and the least squares calculations in Lec18).

—Tom Loredo