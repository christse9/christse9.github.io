The **Inverse Matrix** $A^{-1}\in M_{n}$ is the matrix that, for a matrix $A\in M_{n}$:

$$
A^{-1}A=AA^{-1}=I_{n}
$$

# Finding the inverse

Before any search for the inverse, **first prove det(A) != 0**.

There are many methods used for finding the inverse.

### Adjugate matrix formula

Formally, the inverse of the matrix is calculated as:
$A^{-1}=\frac{1}{\det(A)}adj(A)$
Where adj(A) is the **adjugate matrix.**

The adjugate matrix is in turn defined as the **transpose** of the **cofactor matrix**.
$adj(A)=C^{t}$  where $C=(\ (-1)^{r+c}M_{rc}\ )$

For example $A=\begin{pmatrix}1  & 2 \\  3  & 4\end{pmatrix}$:
There exists the cofactor matrix $C=\begin{pmatrix}c_{11} & c_{12} \\  c_{21} & c_{22}\end{pmatrix}$ where $c_{rc}=(-1)^{r+c}M_{rc}$
In this case:
- $c_{11}=(-1)^{2}[4]$
- $c_{12}=(-1)^{3}[3]$
- $c_{21}=(-1)^{3}[2]$
- $c_{22}=(-1)^{4}[1]$

So $C=\begin{pmatrix}4 & -3 \\  -2 & 1\end{pmatrix}$.

Thus, $adj(A)=C^{t}=\begin{pmatrix}4 & -2 \\  -3 & 1\end{pmatrix}$
As $\det(A)=4-6=-2$:

$A^{-1}=\frac{1}{-2}\begin{pmatrix}4 & -2 \\  -3 & 1\end{pmatrix}=\begin{pmatrix}-2 & 1 \\  \frac{3}{2} & -\frac{1}{2}\end{pmatrix}$

To confirm: $\begin{pmatrix}-2 & 1 \\  1.5 & -0.5\end{pmatrix}\begin{pmatrix}1 & 2 \\  3 & 4\end{pmatrix}=\begin{pmatrix}-2+3 & 2-2 \\  1.5-1.5 & 3-2\end{pmatrix}=\begin{pmatrix}1 & 0 \\  0 & 1\end{pmatrix}=I$
Similarly,
$\begin{pmatrix} 1 & 2 \\  3 & 4\end{pmatrix}\begin{pmatrix}-2 & 1 \\  1.5 & -0.5\end{pmatrix}=I$

Therefore, $A^{-1}=\begin{pmatrix}-2 & 1 \\  1.5 & -0.5\end{pmatrix}$.

### Gaussian Elimination

This is the preferred process for finding the inverse of a higher-dimension matrix, as it is faster.

