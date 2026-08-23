[[02 Linear Algebra]]
# Addition

$+:M\times M\to M$

If $A=(a_{ij})$ and $B=(b_{ij})$ are both in $M_{m\times n}$
Then $A+B=(a_{ij}+b_{ij})$

Elements of the same position in the matrix get added together.

Properties of addition:
- Commutative: A+B=B+A
- Associative: (A+B) + C = A + (B+C)
- Neutral property: The zero matrix $O = (0_{ij})$ | $A+O=A$
- Additive inverse: $A + (-A) = O$
- 

$\begin{pmatrix}1 & 0 \\  0 & 1\end{pmatrix}+\begin{pmatrix}1 & 1 \\  0 & 0\end{pmatrix}=\begin{pmatrix}2 & 1 \\  0 & 1\end{pmatrix}$

# Scalar Multiplication

$*:\mathbb{C}\times M\to M$

If $c$ is a scalar and $A=a_{ij}$
Then $cA=(ca_{ij})$

Properties of scalar multiplication:
- Associative
- Distributive: c(A+B) = cA + cB
- Neutral element: The Identity Matrix $1=\begin{pmatrix}1 & 0 & \dots & 0 \\  0 & 1 & \dots & 0 \\  \dots & \dots & \dots & 0 \\  0 & 0 & 0 & 1\end{pmatrix}$
- Multiplicative property with zero: $0\times A = O$

---

Later on in [[03 Vector Spaces]], you can see that with the above two operations, you can make the space of $m\times n$ matrices into a vector space over a field.

---

# Matrix Multiplication

$*:M_{m\times n}\times M_{n\times p}\to M_{m\times p}$

Matrix multiplication takes a matrix m rows with **n columns** with a matrix of **n rows** and p columns and produces a matrix of m rows and p columns.

$AB=C$

To calculate each element of the new $m\times p$ matrix:
$$
(c_{ij}) = \sum_{k=1}^n a_{ik}\cdot b_{kj}
$$

Below is the multiplication of a $1\times 2$ matrix with a $2 \times 1$ matrix.
$$
\begin{pmatrix}
1 & 2 \\
\end{pmatrix}
\begin{pmatrix}
3 \\
4
\end{pmatrix}
=
(1*3+2*4)=(11)
$$
The result was a $1 \times 1$ matrix.
It only has one element, so the formula gave the sum:
$a_{i 1}b_{1j} + a_{i 2}b_{2j}=1\cdot 3 + 2\cdot 4 = 11$

Imagine the reverse:
$$
\begin{pmatrix}
3 \\
4
\end{pmatrix}
\begin{pmatrix}
1 & 2
\end{pmatrix}
=
\begin{pmatrix}
3\cdot 1 & 3\cdot 2 \\
4\cdot 1 & 4 \cdot 2
\end{pmatrix}
=
\begin{pmatrix}
3 & 6 \\
4 & 8
\end{pmatrix}
$$
Or the following multiplication of 2x2s:
$$
\begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}
\begin{pmatrix}
5 & 6 \\
7  & 8
\end{pmatrix}
=
\begin{pmatrix}
1\cdot 5 + 2 \cdot 7 & 1 \cdot 5 + 2 \cdot 8 \\
3 \cdot 5 + 4 \cdot 7 & 3 \cdot 6 + 4 \cdot 8
\end{pmatrix}
$$
The pattern to be noticed here is that for each element $c_{ij}$,
you multiply one by one,
the elements of row $i$ of the first matrix with the column $j$ of the second matrix,
and finally sum them up.

Properties of Matrix Multiplication:
- (AB)C = A(BC)
- A(B+D)=AB+AD
- (B+D)C=BC+DC
- OA=O' ---- (O: kxm, O': kxn. The dimensions do not stay the same.)
- A(-B)=(-A)B=-AB
- k(AB)=(kA)B=A(kB)

# Matrix Transpose
$t:M_{m\times n}\to M_{n\times m}$

If $A=(a_{ij})\in M_{m\times n}$
Then $A^T=(a_{ji}) \in M_{n\times m}$

Example:

$A=\begin{pmatrix}3-2i & 7\end{pmatrix} \to A^t=\begin{pmatrix}3-2i \\  7\end{pmatrix}$

Every element is **mirrored** across the diagonal.

# Complex conjugate.
$*:M\to M$
If $A = (a_{ij})\in M$
Then $A^*=(a_{ij}^*)$

$A=\begin{pmatrix}3-2i & 7\end{pmatrix} \to A^*=\begin{pmatrix}3+2i & 7\end{pmatrix}$

Every element is **the complex conjugate** of itself.

# Conjugate Transpose

$\dagger:M_{m\times n}\to M_{n\times m}$
If $A=(a_{ij})\in M_{m\times n}$
Then $A^{\dagger}=(a_{ji}^{*})\in M_{n\times m}$

$A=\begin{pmatrix}3-2i & 7\end{pmatrix} \to A^{\dagger}=(A^{*})^{t}=(A^{t})^{*}=\begin{pmatrix}3+2i \\  7\end{pmatrix}$

Every element is **mirrored** AND **the complex conjugate** of themselves.

[[02B Types of Matrices]]


# Questions
 get used to doing these fast:
1) $2\begin{pmatrix}0 & 2 & 3 \\  4 & 0 & 0\end{pmatrix}\begin{pmatrix}1 & 0 \\  0 & 0 \\ 5 & 6\end{pmatrix}= \ ?$
2) $\begin{pmatrix}1-2i & i \\  0 & 1\end{pmatrix}^{\dagger}\begin{pmatrix}1-2i & i \\  0 & 1\end{pmatrix}$
3) Let $$ A= \begin{pmatrix} 1&2\\ a&3 \end{pmatrix}, \qquad B= \begin{pmatrix} 2&-1\\ 1&b \end{pmatrix}. $$ Find all $a,b\in \mathbb{R}$ such that $$ AB=BA. $$
4) 