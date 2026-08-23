[[02 Linear Algebra]]
[[02B Types of Matrices]]

Let a square matrix $A\in M_{n}(K)$ and $k\in \mathbb{Z}$.
Then, the **k-th power** of matrix A, denoted as $A^{k}$, is defined inductively from the equations:
- $A^{0}=I$
- $A^{k}=AA^{k-1}=A^{k-1}A$

For $A,B\in M_{n}(K)$ and $k,l\in \mathbb{Z}$
- $A^{k}A^{l}=A^{k+l}$
- $(A^{k})^{l}=A^{kl}$

If $AB=BA$:
- $A^{k}B^{l}=B^{l}A^{k}$
- $(A+B)^{2}=A^{2}+2AB+B^{2}$
- $(A+B)(A-B)=A^{2}-B^{2}$


# Question

Let
$A=\begin{pmatrix}1&1\\0&1\end{pmatrix}$
Compute $A^2-3A+2I.$
Then, determine $A^n$.

---

The Fibonnaci sequence defines two base values, $F_{1}=1$ and $F_{0}=0$,
and then every other element in the sequence is defined by $F_{n}= F_{n-1}+F_{n-2}$.

Mathematically, it can be proven that this sequence can be described with the following matrix equation:
$$
\begin{pmatrix}
F_{n} \\
F_{n-1}
\end{pmatrix}
=
\begin{pmatrix}
1 & 1 \\
1 & 0
\end{pmatrix}^{n-1}
\begin{pmatrix}
F_{1} \\
F_{0}
\end{pmatrix}
$$
Find $F_{17}$.

With the method you used in the above exercise, how many multiplications would you really need to do to calculate the $2^{30}+1th$ fibonacci number?

---


[[02E Determinant]]