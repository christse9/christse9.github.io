# The concept of a structure

An algebraic structure is a **set** together with one or more **operations** that satisfy **axioms**.

The key idea is:
- The **set** gives the objects 
- An **operation** says how to combine them.
- An **axiom** provides the *rules* which the set and operations obey.

The notation of an algebraic structure is (Set, Operations)

An example is the structure of arithmetic $(\mathbb{R},+,*)$we intuitively use.
The **set** is the set of **real numbers**, $\mathbb{R}$
One of the defined **operations** is **addition** $+$
One of the axioms is $(a+b) + c = a + (b+c)$

# Sets and Operations

A **Set** is just a collection of objects, like numbers.
An **Operation** works like a *function of one or more objects*, which produces another object.

Continuing on the above example, suppose we choose define the operation addition over the natural numbers $\mathbb{N}$.
$$+: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$$
The above notation is read as so: **Addition** is an operation that takes **two elements** from the **set $\mathbb{N}$** and produces an object that **belongs in the same set** $\mathbb{N}$.

###### Open/Closed

As the operation takes inputs from a set, and produces an output that belongs *in the same set*, we say "The set $\mathbb{N}$ is **closed** under that operation".

A set that is **open** under an operation, as follows, takes inputs from some sets, and produces an output that *does not belong in the same sets*.

An example of an open operation over a set is division $\div$ on the set of integers $\mathbb{Z}$.
$2,1\in \mathbb{Z}$. However, $1 \div 2 = 0.5 \not\in \mathbb{Z}$.

###### External/Internal

An **internal** operation takes elements from the same set.
An **external** operation takes elements from different sets.

e.g., imagine a real number multiplying an imaginary number.
$\times:\mathrm{Im}\times \mathrm{Re}\to \mathrm{Im}$
$6\times 2i = 12i$.
Common multiplication with real numbers in a set of imaginaries is an external operation.

**All external operations are open**, because they produce an element that only belongs in one of the two sets.


# Algebraic Axioms

An **Algebraic Axiom** provides a rule that operations follow.
They should **not** be confused with *logical axioms*, e.g.:
if $a=b$ and $b=c$ then $a=c$

The axioms in a structure are *strictly about the operations*.
Above, we called a set **closed** under an operation, because it satisfied what we call the **Closure axiom**: $\forall x,y\in \mathbb{N}\to(x+y)\in \mathbb{N}$.
If x,y in N, then (x+y) is also in N

[[01A Classifications of Algebraic Structures]]


# Questions
1. Prove that the set of Integers $\mathbb{Z}$, defined with the operations of common addition and multiplication $(+,\times)$ is not a Field.
2. Examine if $\mathbb{R}-\{0\}$ defined with the operation $\oplus:a\oplus b=\frac{ab}{2}$ is a Group.
3. Suppose you have a set $A=\{-1,0,1,2\}$.
   Examine if it is a Semi-Group over common addition, and over common multiplication.

4. Examine if the set $A$ of the linear functions $f(x)=a_{0}+a_{1}x, \ a_{0},a_{1}\in \mathbb{R}$ is an Abelian Group over common addition.
   (more specifically) $A=\{f(x)=a_{0}+a_{1}x /a_{i}\in \mathbb{R}\}$

5. Examine if the set $A = \{(x,y,z) \in \mathbb{R}^3 / 2y-z=3x-2\}$ is an Abelian Group over common vector addition.
				Common vector addition: $(x_{1},y_{1})+(x_{2},y_{2})=(x_{1}+x_{2},\  y_{1}+y_{2})$

---

[[02 Linear Algebra]]
