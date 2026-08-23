We said in [[02 Linear Algebra]] that one of the main uses of a matrix is to organize linear equations, turning the following:

$a_{1}x_{1}+a_{2}x_{2}+a_{3}x_{3}=z_{1}$
$b_{1}x_{1}+b_{2}x_{2}+b_{3}x_{3}=z_{2}$
$c_{1}x_{1}x+c_{2}x_{2}+c_{3}x_{3}=z_{3}$

into: $\begin{pmatrix}a_{1} & a_{2} & a_{3} \\  b_{1} & b_{2} & b_{3} \\  c_{1} & c_{2} & c_{3}\end{pmatrix} \begin{pmatrix}x_{1} \\  x_{2} \\  x_{3}\end{pmatrix}=\begin{pmatrix}z_{1} \\  z_{2} \\  z_{3}\end{pmatrix}$

We name the matrix $A=\begin{pmatrix}a_{1} & a_{2} & a_{3} \\  b_{1} & b_{2} & b_{3} \\  c_{1} & c_{2} & c_{3}\end{pmatrix},X=\begin{pmatrix}x_{1} \\  x_{2} \\  x_{3}\end{pmatrix},B=\begin{pmatrix}z_{1} \\  z_{2} \\  z_{3}\end{pmatrix}$
So the system can be symbolized simply as:
$AX=B$

Truly, A is a 3x3, X is 3x1, so the resulting matrix is a 3x1, and each element of the resulting B matrix is following $a_{1}x_{1}+a_{2}x_{2}+a_{3}x_{3}=z_{1}$.

So these matrices produce that system of equations.

# Gaussian Elimination in a system of equations
It can be compressed further by not noting the variables, as $[A|B]$.

If we reduce A to a matrix like $\begin{pmatrix}1 & 0 & 0 \\  0 & 1 & 0 \\  0 & 0 & 1\end{pmatrix}$, then the system of equations would become x1 = z1', x2=z2', x3 = z3', giving us the solution directly.

Row operations work, because they are already used in the solutions of such systems.

$\begin{matrix}2x+y=3 \\  x-y=3\end{matrix}\xrightarrow{R_{1}\to R_{1}+R_{2}}\begin{matrix}3x=6 \\ x-y=3 \end{matrix}\to \dots\to \begin{matrix}x=2 \\  y=-1\end{matrix}$

So it's the same as doing row operations on $\begin{bmatrix}2 & 1 & | & 3 \\  1 & -1 & | & 3\end{bmatrix}$ until the left side reduces to 1s and 0s.

# Echelon and reduced echelon form

An echelon form would be $\begin{pmatrix}1 & * & * \\  0 & 1 & * \\  0 & 0 & 1\end{pmatrix}$ or $\begin{pmatrix}1 & * & * \\  0 & 1 & * \\  0 & 0 & 0\end{pmatrix}$
A reduced echelon form would be $\begin{pmatrix}1 & 0 & 0 \\  0 & 1 & 0 \\  0 & 0 & 1\end{pmatrix}$ or $\begin{pmatrix}1 & 0 & * \\  0 & 1 & * \\  0 & 0 & 0\end{pmatrix}$
As long as the columns of the

**Every invertible coeffficient matrix can be reduced to $I$**.
As for why non-invertible matrices cannot be reduced to the identity matrix, we need to look at the concept of a rank.

# Matrix Rank

The rank of a matrix is equal to the number of non-zero rows in its reduced echelon form.

if a matrix $A$ gets reduced to $\begin{pmatrix}1 & 0 & 0 \\  0 & 1 & 0 \\  0 & 0 & 1\end{pmatrix}$, then it has 3 rows which cannot be reduced further, and so $rank(A)=3$

Another matrix which gets reduced to something like $\begin{pmatrix}1 & 0 & * \\  0 & 1 & * \\  0 & 0 & 0\end{pmatrix}$, then its rank is 2, because its 3rd row is zeroes.

The rank of a matrix informs us of a few things:
- The invertibility of the matrix. If the rank of a matrix is less than its dimension, then through row operations, one of the rows can be turned into zeroes, so its determinant is zero -> not invertible
- The amount of solutions in a system of equations.

If we think of the rows as equations like in a coefficient matrix, then the rank tells us how many independent equations exist.
if $A=\begin{pmatrix}2 & 2 \\  1 & 1\end{pmatrix}$, then it has $rank(A)=1$, and we can see that the top equation is just 2x the bottom one, not any different.
So rank is useful concept for systems.

# Number of solutions in a system of equations - Rouche-Capelli theorem

Let $A\in M_{m\times n}$
### if $rank(A)<rank[A|B]$:
Then the system has **no solutions**.
$\begin{pmatrix}1 & 2 \\  0 & 0\end{pmatrix}X=\begin{pmatrix}3 \\  8\end{pmatrix}$

$rank(A)=1<2=rank([A|B])$, and this is obvious, as the equation is 0x + 0y = 8.

### if $rank(A)=rank([A|B])$
Then the system has **at least one solution**.

- If $rank(A)=n$: Exactly as many columns as rank | **UNIQUE SOLUTION**
- If $rank(A)<n$: More columns than rank | **INFINITE SOLUTIONS**

e.g.
$A=\begin{pmatrix}1 & 2 & 3 \\  0 & 2 & 0\end{pmatrix}$
You have more variables than equations, so even if you find the value of one, say $y$, you'll be left with an equation of the form $x+3z=b$, there are infinite solutions.

---
If there is only one solution, then: $Ax=b\to x=A^{-1}b$, so $A^{-1}$ exists.
This means that if you have a square matrix, then proving $\det(A)\neq 0$ is proof that there exists a unique solution for your system.

---

In short:
$$
\begin{matrix}
r_{A}<r_{Aug} & \to & \text{No solution} \\
r_{A}=r_{Aug}=n & \to & \text{Unique Solution} \\
r_{A}=r_{Aug}<n & \to & \text{Infinite Solutions}

\end{matrix}
$$
And
$$
A\in M_{n}:rank(A)=n \to A^{-1} \ \text{exists}
$$

# The homogenous system
The homogenous system is the system of equation in the form:
$$
AX=O
$$
There are only two possibilites for this system.
# Solutions
$X=(0,0,0,\dots)$ is always true for this system.

If $rank(A)<n$, then again, there are free variables, so there are infinite solutions, along with the trivial solution.

# Questions
Find the solutions $X$ of this system
$$
\left\{
\begin{aligned}
x + y &= 2 \\
2x - y &= 5
\end{aligned}
\right.
$$

---
$A=\begin{pmatrix}1 & 2 & 3 \\  4 & 8 & 12 \\  0 & 0 & 1\end{pmatrix}$ <--- Find $rank(A)$

---
For every value of a, determine the number of solutions in the following system:
$$ \begin{cases} x+2y-z=1\\ 2x+ay+z=3\\ x+(a+2)y=2 \end{cases} $$
Solve only by analyzing the rank.

---
Let $A$ be a $5\times8$ matrix, and $rank(A)=4$
For $AX=B$, what are the possible number of solutions?

---
Let $A\in M_{m\times n}$ and $rank(A)=rank(A|B)$.

Can $AX=B$ have exactly one solution if $m<n$?

---
(Solution 1 below.)
Let $A\in M_{6}$ and $rank(A)=6$.

If $AX=\begin{pmatrix}1 \\  2 \\  3 \\  4 \\  5 \\  6\end{pmatrix}$, determine everything you can say about the system.
What if $rank(5)=5$?

---

(Solution 2 below.)
Prove the following statement in both directions:
$AX=O$ has only the trivial solution $\leftrightarrow$ A is invertible.

---
# SOLUTIONS FOR SOME OF THE PROBLEMS

1. 
A is a square matrix with $rank(A)=n$, therefore it is invertible.
Thus, there exists a unique solution for $AX=B$. 
The (1 2 3 4 5 6) gives us no information since we do not know the elements of $A$.
If $rank(A)=5<6=n$, then $A$ is not invertible.
Therefore, depending on  $rank([A|B])$ being equal or larger than $rank(A)$, there are either infinite or no solutions.
It cannot produce a unique solution, because there is a free variable in the equation.

2. 
Right to left:
$A$ is invertible
We want to show that $AX=O$ only has the trivial solution $X=(0,\dots)$.
Since $A$ is invertible, $A^{-1}AX=A^{-1}O\to I X=O\to X=O$.

Left to right:
$AX=O$ only has the trivial solution.
We want to show that $A$ is invertible.
Because there are no non-trivial solutions, $rank(A)=n$.
Therefore, it is a square matrix and has full rank.
Therefore, $A$ is invertible.