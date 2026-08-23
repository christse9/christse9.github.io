[[02 Linear Algebra]]
[[02A Matrix Operations]]
# Identity Matrix

The Identity Matrix is a square matrix $m\times m$ whose diagonal is all 1.

$(1), \begin{pmatrix}1 & 0 \\  0 & 1\end{pmatrix}, \begin{pmatrix}1 & 0 & 0 \\  0 & 1 & 0 \\  0 & 0 & 1\end{pmatrix}$ and so on, for each dimension.

It can be defined from the function $\delta_{ij}$ (Delta Kroenecker)
$I=[\delta_{ij}]$ where $\delta_{ij}=\begin{Bmatrix}0, & \forall i\neq j \\  1, & \forall i=j \end{Bmatrix}$

# Zero matrix

The Zero matrix is any matrix of any dimension whose every element is 0.

# Square Matrix

Every matrix who has as many rows as many columns: $m\times m$
Denoted as $A=[a_{ij}], i,j\in[1,n]$

It is called a square matrix of size $n$.
Thus, the set of square matrices size n is denoted $M_{n}$

### Diagonal Matrix
The diagonal matrix is a square matrix thathas non-zero values only across its diagonal.
$D=diag(d_{ii})$

$diag(1,2,3)=\begin{pmatrix}1 & 0 & 0 \\  0 & 2 & 0 \\  0 & 0 & 3\end{pmatrix}$

### Upper/Lower Triangular Matrix
Upper: Entries below the diagonal are zero
Lower: Entries above the diagonal are zero

### Symmetric Matrix
A symmetric matrix is a square matrix $A=[a_{ij}]$ that satisfies:
$A^{t}=A  \leftrightarrow a_{ij}=a_{ji}$

### Anti-Symmetric Matrix
An anti-symmetric matrix is a square matrix $A=[a_{ij}]$ that satisfies:
$A=-A^{t} \leftrightarrow \begin{Bmatrix}a_{ij}= -a_{ji} & \forall i\neq j \\  a_{ii}=0 & \forall i=j\end{Bmatrix}$

### Orthogonal Matrix
An orthogonal matrix is a square matrix whose product with its transpose is commutative and equal to $I$
$AA^{t}=A^{t}A=I$

### Hermitian Matrix
A matrix $M_{n}(\mathbb{C})$ that satisfies:
$A^{*}=A$

### Invertible Matrix
A matrix $A\in M_{n}(K)$ for which exists a matrix $A^{-1}\in M_{n}(K)$:
$AA^{-1}=A^{-1}A=I$

---

[[02C Matrix Exponentiation]]

