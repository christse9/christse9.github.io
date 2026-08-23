The determinant is a function that is defined **only** for square matrices.

The result of this function is a single number associated with it, and as will be shown, it informs us a lot about that matrix's behavior.

For a 2x2 matrix,
$A=\begin{pmatrix}a & b \\  c  & d\end{pmatrix}$,
the determinant is $\det(A)=ad-bc$.

# Geometrical view of the determinant.

In the case of vectors, the determinant is one of the main measurements of how a matrix transforms the space.
Following with the example in [[02D Linear Transformation]], we had a matrix $\begin{pmatrix}2  & 0 \\  0 & 3\end{pmatrix}$ that, as we saw, stretched the x direction to twice its size, and the y direction to thrice its size. Thus, the total increase in scale was 6x.

It's clear that $\det(A)=2\cdot 3 = 6$.

So if a matrix represents how a transformation moves the basis vectors, the determinant is a **signed scale factor** between the old size and the new one.

# Calculating determinants of higher dimension

Suppose a random 3D matrix $A=\begin{pmatrix}a & b & c \\  d & e & f \\  g & h & j\end{pmatrix}$

$$
\det(A)=
a \begin{bmatrix}
e & f \\
h & j
\end{bmatrix}
- b
\begin{bmatrix}
d & f \\
g  & j
\end{bmatrix}
+ c
\begin{bmatrix}
d & e \\
g & h
\end{bmatrix}
$$
The process used deriving the determinant of an n-dimension matrix is solving the sum:

For any row $r$ of a n-dim matrix:
$$
\det(A)=\sum_{c=1}^{n} a_{rc}(-1)^{r+c}M_{rc}
$$
where $M_{rc}$ is the resulting determinant after *deleting* the row $r$ and column $c$.

- $M_{rc}$ is called a **minor** of the matrix $A$
- $(-1)^{r+c}M_{rc}$ is called the **cofactor** of the element at r,c.

In practice, the solution of a multiple-dimension matrix happens through repeatedly reducing it until it's a sum of 2D determinants.

- Pick any row or column.
- Pick the first element in the row/column.
- Calculate sign using its position: $(-1)^{\text{row+column}}$ 
- The first term is that first element * its sign * the remaining matrix deleting its row and column
- Repeat for the next element until you go through the row/column.

The freedom we have in selecting any row/column we want makes calculating determinants have many shortcuts.

Mainly when there exists 0s or 1s within the determinant.

e.g. $\begin{bmatrix}1 & 2 & -49253 \\  0 & 0 & 4 \\  2 & 1 & 99\end{bmatrix}$

Rather than taking the top row, we can choose the middle row and immediately reduce it to just $4 \begin{bmatrix}1 & 2 \\  2 & 1\end{bmatrix}=4(1-4)=-12$

This also quickly shows that **if ANY row or column has only 0s, then the determinant is zero**.

# Value of the determinant

$\det>0$:
- The transformation does not flip space
- If $\det=1$: Area/volume is preserved
- If $\det \neq 1$: Area is **scaled** by that factor

$\det<0$:
- Same function as positive, only also flips space
- Scales by factor $|\det|$

$\det = 0$:
When a determinant is zero, we are informed that the **space collapses**.
What this means is that something like a 3D volume can be transformed into a 2D plane, 1D line, or just a point.

Take for example the transformation $\begin{pmatrix}1 & 0 \\ 0 & 0 \end{pmatrix}$ applied to a 2D space.
As seen in [[02D Linear Transformation#The effect of matrix multiplication|linear transforms]], this maps the x base vector to $\begin{pmatrix}1 \\  0\end{pmatrix}$ and the y base vector to $\begin{pmatrix}0 \\  0\end{pmatrix}$.
This means that every vector in the space that was: $u = ax +by$ becomes $u=ax$.
So something like $\begin{pmatrix}2x \\  5y\end{pmatrix}$ and $\begin{pmatrix}2x \\  3y\end{pmatrix}$ would both get mapped to $\begin{pmatrix}2x \\  0\end{pmatrix}$.

The **entire y dimension** collapses into zero, so information is completely lost.
The entire 2D space collapses into a line, the x axis.

If the matrix happened to be $\begin{pmatrix}0 & 0 \\  0 & 0\end{pmatrix}$ then the space would collapse all to origin point.

Because multiple points get condensed into one, no matter what transformation is applied after, there does not exist a matrix that can **undo** the transformation.
Thus, there is no way to bring back the original vector, infromation is lost.

For example, the transformation of $\begin{pmatrix}2 & 0 \\  0 & 3\end{pmatrix}$ could be inverted by applying $\begin{pmatrix} \frac{1}{2} & 0 \\  0 & \frac{1}{3}\end{pmatrix}$ after.

Thus, if $\det = 0$:
- At least one dimension collapses.
- The matrix is **not invertible**.

[[02F Inverse Matrix]]