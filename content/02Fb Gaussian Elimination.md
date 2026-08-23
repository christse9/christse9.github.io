# The Augmented Matrix

Two matrices put side-by-side is called an augmented matrix.
if $A=\begin{pmatrix}1 & 2 \\  3 & 4\end{pmatrix}$, then the augmented matrix $[A|I]=\begin{pmatrix}1 & 2 & | & 1 & 0 \\  3 & 4 & | & 0 & 1\end{pmatrix}$.

# Gaussian Elimination On an Augmented Matrix

Gaussian Elimination is a process that uses [[02E Determinant#Row and Column Operations|Row operations]] to reduce an augmented matrix's left side to rows like (1, 0, 0). This is used in solving [[02G Systems of Linear Equations]], but in this case, it does the following:
$$[A:I]\xrightarrow{\text{Gaussian Elimination}}[I:A^{-1}]$$
Whatever the right side turns to as we reduce A to the identity matrix, is the inverse matrix.

The general plan is to 

e.g.
$\begin{pmatrix}1 & 2 & | & 1 & 0 \\  3 & 4 & | & 0 & 1\end{pmatrix}\xrightarrow{R_{1}\to 3R_{1}}\begin{pmatrix}3 & 6 & | & 3 & 0 \\  3 & 4 & | & 0 & 1\end{pmatrix}$
$\xrightarrow{R_{2}\to R_{2}-R_{1}}\begin{pmatrix}3 & 6 & | & 3 & 0 \\  0 & -2 & | & -3 & 1\end{pmatrix}\xrightarrow{R_{1}\to R_{1}+3R_{2}}\begin{pmatrix}3 & 0 & | & -6 & 3 \\  0 & -2 & | & -3 & 1\end{pmatrix}$
$\xrightarrow[R_{2}\to \frac{R_{2}}{-2} ]{R_{1}\to \frac{R_{1}}{3}}\begin{pmatrix}1 & 0 & | & -2 & 1 \\  0 & 1 & | & 1.5 & -0.5\end{pmatrix}$



So $A^{-1}=\begin{pmatrix}-2 & 1 \\  1.5 & -0.5\end{pmatrix}$
To confirm: $\begin{pmatrix}-2 & 1 \\  1.5 & -0.5\end{pmatrix}\begin{pmatrix}1 & 2 \\  3 & 4\end{pmatrix}=\begin{pmatrix}-2+3 & 2-2 \\  1.5-1.5 & 3-2\end{pmatrix}=\begin{pmatrix}1 & 0 \\  0 & 1\end{pmatrix}=I$
Similarly,
$\begin{pmatrix} 1 & 2 \\  3 & 4\end{pmatrix}\begin{pmatrix}-2 & 1 \\  1.5 & -0.5\end{pmatrix}=I$
