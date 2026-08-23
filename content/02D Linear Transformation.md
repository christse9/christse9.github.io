[[02 Linear Algebra]]

Linear algebra is heavily used in computer graphics due to one geometrical application of a matrix, linear transformation.

Suppose we have a grid with these 5 points on a 2D.
![[Pasted image 20260823163307.png]]

Thsese points, like vectors, are represented with their two coordinates as $\begin{pmatrix}x \\  y\end{pmatrix}$
$\begin{pmatrix}0 \\  1\end{pmatrix},\begin{pmatrix}0 \\  0\end{pmatrix},\begin{pmatrix}1 \\  0\end{pmatrix},\begin{pmatrix}1 \\  1\end{pmatrix},\begin{pmatrix}0.5 \\  0.5\end{pmatrix}$

Aka, they can be represented as 2x1 matrices. They can also be represented horizontally, like $(0,1)$ and so on, but the standard is vertically.

So suppose now we make up another matrix, like $A=\begin{pmatrix}2 & 0 \\  0 & 3\end{pmatrix}$.

We observe, by multiplying any of those coordinates with this matrix: $\begin{pmatrix}2 & 0 \\  0 & 3\end{pmatrix}\begin{pmatrix}1 \\  1\end{pmatrix}=\begin{pmatrix}2 \\  3\end{pmatrix}$

By repeating this process for every coordinate, the new coordinates become these:
$\begin{pmatrix}0 \\  3\end{pmatrix},\begin{pmatrix}0 \\  0\end{pmatrix},\begin{pmatrix}2 \\  0\end{pmatrix},\begin{pmatrix}2 \\  3\end{pmatrix},\begin{pmatrix}1 \\  1.5\end{pmatrix}$

Through the multiplication with that matrix, we have mapped these coordinates to a new set of coordinates.
![[Pasted image 20260823164620.png#invert]]

In effect, for any point $u=\begin{pmatrix}x \\  y\end{pmatrix}$: $A\cdot u=\begin{pmatrix}2x \\  3y\end{pmatrix}$.
We've discovered that the diagonal matrix $A$ **scales** space when we apply it to every point inside it.

In creating $A$, however, we purposefully left two entries as zero.

In another example, let's make up a matrix $B=\begin{pmatrix}0 & 1 \\  1 & 0\end{pmatrix}$.
If we multiply the original coordinates with B, $\begin{pmatrix}0 & 1 \\  1 & 0\end{pmatrix}\begin{pmatrix}1 \\  0\end{pmatrix}=\begin{pmatrix}0 \\  1\end{pmatrix}$
Its effect is that it **mirrors** coordinates across the line y=x.

# The effect of matrix multiplication

In the above examples, what we effectively saw the linear transform is, is a **mapping** of one set of coordinates to another.

In [[03 Vector Spaces]], the concept of a transformation is more easily explained using the **basis**. The basis is a set of any vectors which, through basic addition, can derive every other vector in the space.
For example, with $x=\begin{pmatrix}1 \\  0\end{pmatrix}$ and $y =\begin{pmatrix}0 \\  1\end{pmatrix}$, 
it is clear that any possibly coordinate can be derived as $a=\begin{pmatrix}2 \\  3\end{pmatrix}=2x+3y$.
Thus, a random matrix $\begin{pmatrix}a  & b \\  c  & d\end{pmatrix}$ will map $\begin{pmatrix}1 \\  0\end{pmatrix}\to \begin{pmatrix}a \\  c\end{pmatrix}$ and $\begin{pmatrix}0 \\  1\end{pmatrix}\to \begin{pmatrix}b \\  d\end{pmatrix}$.

So any coordinate becomes $a=2x+3y=\begin{pmatrix}a+b \\  c+d\end{pmatrix}$.

# The rotation matrix

The rotation matrix in 2D is this: $\begin{pmatrix}\cos \theta & -\sin \theta \\  \sin \theta  & \cos \theta\end{pmatrix}$
This maps coordinates to a rotation θ degrees counter-clockwise around the origin point (0,0), without affecting the scale.

![[Pasted image 20260823194424.png]]

How a matrix affects the scale of the space it's applied to is a property is learned through its [[02E Determinant|determinant]].

# Shear transform
A shear transformation changes the shape, but conserves the area.
![[Pasted image 20260824000457.png#invert]]

# A non-linear transformation
A non-linear transformation cannot be encoded in a matrix, because matrices, by design, are linear.
Thus, transformations in general are described as something like $T(x,y)=(2x,y+3)$
A non-linear transformation would be something like: $T(x,y)=(xy,y))$
xy is not a linear term, so something like this is impossible to describe in linear algebra through a standard matrix.
Thus, different tricks are used. For example, the Jacobian transformation which is used when switching between two coordinate systems, approximates the area locally as linear through calculus infinitesimals.