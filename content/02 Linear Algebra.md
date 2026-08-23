The need for organization of large blocks of data and large systems of equations gave rise to a neat representation of them called a Matrix.

Functionally, it can turn something annoying to write like
$a_{1}x_{1}+a_{2}x_{2}+a_{3}x_{3}=z_{1}$
$b_{1}x_{1}+b_{2}x_{2}+b_{3}x_{3}=z_{2}$
$c_{1}x_{1}x+c_{2}x_{2}+c_{3}x_{3}=z_{3}$

into: $\begin{pmatrix}a_{1} & a_{2} & a_{3} \\  b_{1} & b_{2} & b_{3} \\  c_{1} & c_{2} & c_{3}\end{pmatrix} \begin{pmatrix}x_{1} \\  x_{2} \\  x_{3}\end{pmatrix}=\begin{pmatrix}z_{1} \\  z_{2} \\  z_{3}\end{pmatrix}$

Any information which can fit into a grid can be represented using a matrix.
In physics, data about space, movement and forces, energy, etc. can be put into matrices. 

# Definition of a matrix

A matrix is an **array of elements**: A = $(a_{ij})$
with $m$ **rows** and $n$ **columns**. e.g.
$\begin{pmatrix}1 & 2 \\  3 & 4\end{pmatrix}$, $\begin{pmatrix}1 & -i & -67\end{pmatrix}$

A set of matrices of dimensions $m\times n$ is denoted as $M_{m\times n}$

### Elements, Rows, Columns

Suppose a matrix $A=\begin{pmatrix}1 & 2 \\  3 & 4\end{pmatrix}$
Its **elements** are the values in a given **row**+**column**, denoted by $a_{row|column}$
so in the above matrix, $a_{11}=1,a_{12}=2,a_{21}=3,a_{22}=4$.

To denote a random matrix, $(a_{ij})$ is used to denote all the elements inside it.

When specifying the set the elements belong in, in a set of matrices, it is denoted as so:
$M_{m\times n}(\mathbb{R})$

##### Diagonal
The **Diagonal** is the list of elements in a matrix that are on the diagonal starting topleft.
$diag(A)=(a_{ij}),\ i=j$.

### Trace
The **Trace** is the sum of the diagonal.
$tr(A)=\sum_{i=1}^{n}a_{ii}$

[[02A Matrix Operations]]
[[02B Types of Matrices]]
[[02C Matrix Exponentiation]]
[[02E Determinant]]


[[03 Vector Spaces]] | unfinished