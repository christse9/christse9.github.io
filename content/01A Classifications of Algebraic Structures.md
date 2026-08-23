[[01 Algebraic Structures]]

Depending on which common axioms are defined in a structure, it is given a classification.

### Semi-Group $(A,\oplus)$
- Closure: $a,b\in A \to (a \oplus b)\in A$

- Associative property: $(a \oplus b) \oplus c = a \oplus (b \oplus c)$

### Group $(A,\oplus)$
- Is a *Semi-Group*

- $\exists \ e \in A: \forall a \in A, a \oplus e = e \oplus a = a$
	$e:$ A **neutral element** of the operation $\oplus$. *Unique.*

- $\exists \ a' \in A: \forall a\in A, a\oplus a' = e$.
	$a':$ A **symmetrical element** of the operation $\oplus$. *Unique for each element*.

### Abelian Group $(A,\oplus)$
- Is a *Group*

- Commutative property: $a \oplus b = b \oplus a$

### Ring $(A,\oplus,\otimes)$
- In the *Abelian group* $(A,\oplus)$ is defined a second operation $\otimes$.

- Associative Property of $\otimes$: $(a\otimes b)\otimes c=a\otimes(b\otimes c) \ \ \forall a,b,c\in A.$

- Distributive property from the left: $a\otimes (b\oplus c) = (a\otimes b) \oplus (a\otimes c)$

- Distributive property from the right: $(b\oplus c)\otimes a = (b\otimes a) \oplus (c \otimes a)$ 
	*The commutative property is NOT necessarily true here ^^^*

- $\exists \ e' \in A-\{e\}: \forall a\in A, e'\otimes a = a \otimes e' = a$
	$e':$ A **neutral element** of the operation $\otimes$. *Unique for all. MUST be different from e.*

### Commutative Ring $(A, \oplus, \otimes)$
- Is a *Ring* $(A,\oplus,\otimes)$

- Commutative property for $\otimes$: $a \otimes b = b \otimes a$

### Field $(A,\oplus, \otimes)$
- Is a *Commutative Ring* $(A,\oplus,\otimes)$

- $\exists \ a'',a \in A-\{e\}: a\otimes a''=a''\otimes a=e'$
	$a'':$ A **symmetrical element** of the operation $\otimes$. *Unique for each. Must be different from e and e'.


Example:
The set of real numbers defined with common addition and multiplication is a Field,
where:
- e=0: neutral element of addition
- e=1: neutral element of multiplication
- a'=(-a): symmetrical element of addition
- a''=(1/a): symmetrical element of multiplication

Those operations and common sets like $\mathbb{Q},\mathbb{R},\mathbb{C}$ are Fields.

