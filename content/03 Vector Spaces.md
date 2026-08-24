unfinihsed

---

# Defining vectors

A **vector** is traditionally an object in *coordinate geometry* that has **magnitude and direction**.
Algebraically, it is any object that contains a list of numbers.
The contrast with normal numbers (scalars) is that they only have magnitude, aka they only contain 1 number.
Written as an *ordered list of numbers* $(1,-2)$, meant to describe the **components in a coordinate system**, these vectors are defined properly in an algebraic structure known as a **Vector Space**.

Geometrically, when connecting two points, they are written as $\vec{AB}$.
Generally, they are denoted as variables with an arrow $\vec{a}$.

For convenience, here they'll be denoted by ijk, uv, xyz, without arrows, while abcd, will be scalars.

# Vector Space
A vector space is an algebraic structure that consists of:
- A set of vectors $V$
- A **field** of scalars $F$
- A binary operation $V\times V \to V$
- An external operation $F\times V \to V$

The binary operation is common vector addition.
$(x,y)+(x',y')=(x+x', y+y')$

The external operation is scalar multiplication.
$3(x,y)=(3x,3y)$

The vectors satisfy all the different axioms mentioned in [[01A Classifications of Algebraic Structures|here]] in their own way, but because one of the operations are external, it can't be called a field.
This means they satisfy axioms like associativity, distributivity, a zero vector, inverses, etc.

As will be seen later on, as vectors can have as many dimensions as they want, and linear equations describe many physical systems, vector spaces are heavily used in physics and quantum mechanics.

Examples of vector spaces include $\mathbb{R}^2$, the two-dimensional cartesian vector space, and similarly $\mathbb{R}^3$, the 3D one.

![[Pasted image 20260819212030.png|#invert]]

The above is a geometric representation of a vector $\vec{OP}$ in $\mathbb{R}^3$.

The arrows $i,j,k$ are called **basis** vectors of the coordinate system.

# Linear combinations, span and independence

A **linear combination** is the addition of vectors each with whatever coefficient:
$a_{1}v_{1}+a_{2}v_{2}+\dots+a_{n}v_{n}$
where $a_{i}\in F,u_{i}\in V$

The **span** of a set of vectors is the set of all linear combinations of them.
E.g. the vectors $(1,0,0)$ and $(0,1,0)$ have a span containing every vector $(a,b,0)$ where $a,b\in F$.

**Linear Independence** is when the ONLY solution to the below equation:
$a_{1}v_{1}+a_{2}v_{2}+\dots+a_{n}v_{n}=0$
is when all coefficients are zero.

# Basis and dimension

A **basis** is the smallest useful set of vectors from which every other vector in the space can be built by **linear combination**.

The **dimension** is the number of vectors in a basis of a finite-dimensional space.
e.g.
$\mathbb{R}^3$ has the basis: $(1,0,0),(0,1,0),(0,0,1)$
Its dimension is 3.

Both finite and infinite-dimensional vector spaces are needed for quantum mechanics.
