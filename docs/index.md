---
layout: default
title: MA1508E
---
# MA1508E Formulae, Theorems and Definitions

## Note
* I have added in parentheses (...) some additional keywords at some headers for easier lookup for some theorems/definitions/formulae.
* If there are any more defintions or theorems you wish to add, create an issue or let me know directly!
* There are **VERY** important lists/properties I have compiled [here](...), and have also scattered the link throughout the document to send you there directly, but they are also in their own individual sections.

## Table of Contents

1. **[Chapter 1: Linear Systems](#linear-systems)**
2. **[Chapter 2: Matrix Algebra](#matrix-algebra)**
3. **[Chapter 3: Euclidean Vector Spaces](#euclidean-vector-spaces)**
4. **[Chapter 4: Subspaces Associated to a Matrix](#subspaces)**
5. **[Chapter 5: Orthogonality, Projection, and Least Square Solution](#orthogonality-projection-and-lss)**
6. **[Chapter 6: Eigenanalysis](#eigenanalysis)**
7. **[Chapter 7: System of Linear Differential Equations](#system-of-linear-differential-equations)**

<div style="page-break-after: always;"></div>

## Linear Systems

### Consistent and Inconsistent Linear Systems

An inconsistent linear system has **no solutions**, whereas a consistent linear system has **at least one solution**.

### Row Echelon Form

1. If there are zero rows, they are at the bottom of the matrix.
2. Leading entries are further to the right as we move down the matrix.

### Reduced Row Echelon Form

Adding on to 1. and 2.,

3. The leading entries are all 1.
4. In each pivot column, all entries except the leading entry is 0.

### Row Equivalent Matrices

* Two (augmented) matrices are **row equivalent** if one can be obtained from the other by performing a set of *
  *elementary row operations**.
* Two linear systems have the **same solutions** if their augmented matrices are **row equivalent**.
    * Their rref forms are the same &#8594; same solution

<div style="page-break-after: always;"></div>

## Matrix Algebra

### Properties of Matrix Addition and Scalar Multiplication

* **A** + **B** = **B** + **A** (Commutative)
* **A** + (**B** + **C**) = (**A** + **B**) + **C** (Associative)
* **0** + **A** = **A** (Additive Identity)
* **A** + (-**A**) = **0** (Additive Inverse)
* _a_(**A** + **B**) = _a_**A** + _a_**B** (Distributive Law)
* (_a_ + _b_)**A** = _a_*A* + _b_**A** (Scalar Addition)
* (_ab_)**A** = _a_(_b_**A**) (Associative)
* If _a_**A** = **0**, then either _a_ = 0 or **A** = **0**

### Properties of Matrix Multiplication

* (**AB**)**C** = **A**(**BC**) (Associative)
* **A**(**B** + **C**) = **AB** + **AC** (Left Distributive Law)
* (**A** + **B**)**C** = **AC** + **BC** (Right Distributive Law)
* _c_(**AB**) = (_c_**A**)**B** = **A**(_c_**B**) (Commute with scalar multiplication)
* For any _m x n_ matrix **A**, **I<sub>m</sub>A** = **A** = **AI<sub>n</sub>**
* If **AB** = **0**<sub>m x n</sub>, **A** and **B** can both be **nonzero**

### Properties of Transpose

* (**A**<sup>*T*</sup>)<sup>*T*</sup> = **A**
* (_c_**A**)<sup>*T*</sup> = _c_**A**<sup>*T*</sup>
* (**A** + **B**)<sup>*T*</sup>= **A**<sup>*T*</sup> + **B**<sup>*T*</sup>
* (**AB**)<sup>*T*</sup> = **B**<sup>*T*</sup>**A**<sup>*T*</sup>
* If **A** is **symmetric**, **A**<sup>*T*</sup> = **A**

### Block Multiplication
$$
\begin{aligned}
AB &= A \begin{pmatrix} \mathbf{b}_1 & \mathbf{b}_2 & \cdots & \mathbf{b}_n \end{pmatrix}
= \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 & \cdots & A\mathbf{b}_n \end{pmatrix} \\
\\
AB &=
\begin{pmatrix}
\mathbf{a}_1 \\
\mathbf{a}_2 \\
\vdots \\
\mathbf{a}_m
\end{pmatrix}
B =
\begin{pmatrix}
\mathbf{a}_1 B \\
\mathbf{a}_2 B \\
\vdots \\
\mathbf{a}_m B
\end{pmatrix}
\end{aligned}
$$



### Invertible Matrices

[Final Invertible List](...)

### Properties of Invertible Matrices

Let **A** be an invertible matrix of order n.

* (**A**<sup>-1</sup>)<sup>-1</sup> = **A**
* (*a***A**)<sup>-1</sup> = $\frac{1}{a}$**A**<sup>-1</sup>
* (**A**<sup>*T*</sup>)<sup>-1</sup> = (**A**<sup>-1</sup>)<sup>*T*</sup>
* (**AB**)<sup>-1</sup> = **B**<sup>-1</sup>**A**<sup>-1</sup>

### Elementary Matrices

* If **B** is row equivalent to **A**, **B** = **E<sub>k</sub>...E<sub>2</sub>E<sub>1</sub>A**.

### Inverse of Elementary Matrices

* **E**: *R<sub>i</sub>* + *cR<sub>j</sub>*, **E**<sup>-1</sup>: *R<sub>i</sub>* - *cR<sub>j</sub>*
* **E**: *R<sub>i</sub>* ↔ *R<sub>j</sub>*, **E**<sup>-1</sup>: *R<sub>i</sub>* ↔ *R<sub>j</sub>* (same matrix!)
* **E**: *cR<sub>i</sub>*, **E**<sup>-1</sup>: $\frac{1}{c}$*R<sub>i</sub>*

### Determinant

* For 2×2 matrices, **A** = $ \begin{pmatrix} a & b  \\ c & d  \end{pmatrix} $ $\det(\mathbf{A}) = ad - bc$.
* For higher powers, use cofactor expansion (Remember to check the sign!):

  $$ 
  \begin{pmatrix}
  + & - & + & \cdots & \cdots \\
  - & + & - & \cdots & \cdots \\
  + & - & + & \cdots & \cdots \\
  \vdots & \vdots & \vdots & \ddots & \vdots \\
  \cdots & \cdots & \cdots & \cdots & \cdot
  \end{pmatrix}
  $$ 

### Properties of Determinant

Let **A** and **B** be a square matrices of the same order.

* det(**A**) = det(**A**<sup>*T*</sup>)
* If **A** is triangular, det(**A**) = *a<sub>11</sub>a<sub>22</sub>...a<sub>nn</sub>*
    * Multiply all its diagonal entries
* det(**A**<sub>1</sub>**A**<sub>2</sub>...**A**<sub>k</sub>) = det(**A**<sub>1</sub>)det(**A**<sub>2</sub>)...det(**A**<sub>k</sub>)
* det(**A**<sup>-1</sup>) = det(**A**)<sup>-1</sup>
* det(*c***A**) = *c*<sup>*n*</sup>det(**A**)

### Determinant of Elementary Row Operations

* **E**: *R<sub>i</sub>* + *cR<sub>i</sub>* → det(**E**) = 1
* **E**: *R<sub>i</sub>* ↔ *R<sub>i</sub>* → det(**E**) = -1
* **E**: *cR<sub>i</sub>* → det(**E**) = c

<div style="page-break-after: always;"></div>

## Euclidean Vector Spaces

### Dot Product
Also known as **inner product**
* **u** $\cdot$ **v** = **u**<sup>*T*</sup>**v**
* **u** $\cdot$ **v** = *u*<sub>1</sub>*v*<sub>1</sub> + *u*<sub>2</sub>*v*<sub>2</sub> + ... + *u*<sub>*n*</sub>*v*<sub>*n*</sub>

Angle definition for Dot Product
* $\cos(\theta) = \frac{\mathbf{u} \cdot \mathbf{v}}{\lVert \mathbf{u} \rVert \lVert \mathbf{v} \rVert}$

### Norm (or Magnitude)
* $\lVert\mathbf{u}\lVert$ = $\sqrt{\mathbf{u} \cdot \mathbf{u}}$ = $\sqrt{\mathbf{u}_1^2 + \mathbf{u}_2^2 + \cdots + \mathbf{u}_n^2}$

### Properties of Inner Product and Norm
* **u** $\cdot$ **v** = **v** $\cdot$ **u**
* *c* **u** $\cdot$ **v** = (*c* **u**) $\cdot$ **v** = **u** $\cdot$ (*c* **v**)
* **u** $\cdot$ (*a* **v** + *b* **w**) = *a* **u** $\cdot$ **v** + *b* **u** $\cdot$ **w**
* **u** $\cdot$ **u** $\geq$ 0
    * **u** $\cdot$ **u** = 0 *if and only if* **u** = **0**
* $\lVert$*c* **u**$\lVert$ = $\mid$*c*$\mid$ $\lVert$**u**$\lVert$

### To check for Linear Combination
* (**u**<sub>1</sub> **u**<sub>2</sub> ... **u**<sub>k</sub> $\mid$ **v**) is **consistent**

### To check if span(S) = $\mathbb{R}^n$
* *rref*(**u**<sub>1</sub> **u**<sub>2</sub> ... **u**<sub>k</sub>) has no zero rows

### Properties of Linear Spans
1. Zero vector **0** is in span(*S*)
2. $\alpha$ **u** $\in$ span(*S*)
3. **u** + **v** $\in$ span(*S*)<br>

We can combine 2. and 3. and check: $\alpha$ **u** + $\beta$ **v** $\in$ span(*S*) (sometimes this is harder though, so just pick whichever is easier)

### To check for Set Relations between Spans
* (**u**<sub>1</sub> **u**<sub>2</sub> ... **u**<sub>*S*</sub> $\mid$ **v**<sub>1</sub> $\mid$ **v**<sub>2</sub> $\mid$ ... $\mid$ **v**<sub>*T*</sub>) is **consistent** → span(*T*) $\subseteq$ span(*S*)

### Subspaces
If **V** is a *subspace*:
1. Zero vector **0** is in **V**
2. $\alpha$ **u** $\in$ **V**
3. **u** + **v** $\in$ **V**<br>

We can combine 2. and 3. and check: $\alpha$ **u** + $\beta$ **v** $\in$ **V** (sometimes this is harder though, so just pick whichever is easier)
 * Further notes:
    * We can express **V** = span(*S*) for some finite set *S* (**IMPT and useful result**)
    * Only **homogeneous** linear systems are subspaces (i.e. **Ax** = **b**, where **b** = **0**)

### Linear Independence
Let *S* = {**u**<sub>1</sub>, **u**<sub>2</sub>, ..., **u**<sub>*k*</sub>}, then *S* is **linearly independent** if:
* *c*<sub>1</sub>**u**<sub>1</sub> + *c*<sub>2</sub>**u**<sub>2</sub> + ... + *c*<sub>*k*</sub>**u**<sub>*k*</sub> = **0** can only be satisfied by *c*<sub>1</sub> = *c*<sub>2</sub> = ... = *c*<sub>*k*</sub> = 0
    * *rref*(*S*) = **I** → *S* is **linearly independent**

### To check for linear independence
Let *S* = {**u**<sub>1</sub>, **u**<sub>2</sub>, ..., **u**<sub>*k*</sub>}
* *rref*(*S*) has **no non-pivot columns**

### Basis
A set *S* is a basis for **V** if:
* span(*S*) = **V**
* *S* is linearly independent

Note: The basis of a zero space {**0**} is the empty set $\emptyset$

### Other ways to check for Basis
* B1
    * $\mid$*S*$\mid$ = *dim*(*V*)
    * *S* $\subseteq$ *V*
    * *S* is linearly independent
* B2
    * $\mid$*S*$\mid$ = *dim*(*V*)
    * *V* $\subseteq$ span(*S*)

### Coordinates relative to a Basis (or Set)
Let *S* = {**u**<sub>1</sub>, **u**<sub>2</sub>, ..., **u**<sub>*k*</sub>} be a basis for *V*, and **v** = *c*<sub>1</sub>**u**<sub>1</sub> + *c*<sub>2</sub>**u**<sub>2</sub> + ... + *c*<sub>*k*</sub>**u**<sub>*k*</sub> be the **unique** representation of **v** $\in$ *V*
![coordinates_basis](images/coordinates_basis.png)

### To compute coordinates relative to a Basis (or Set)
* Solve the linear system: (**u**<sub>1</sub> **u**<sub>2</sub> ... **u**<sub>*k*</sub> $\mid$ **v**)

### Dimensions
* *dim*(*V*): Number of vectors in any *basis* of *V*
* *dim*({**0**}) = 0

<div style="page-break-after: always;"></div>

## Subspaces Associated to a Matrix

### Row Operations Preserve Row Space
* If **A** and **B** are row equivalent matrices, Row(**A**) = Row(**B**)

### Finding Basis for Row Space
Let **A** be a matrix, with **R** being its *rref* form.
* Basis of Row(**A**) is the nonzero rows of *rref*(**A**) **OR** nonzero rows of **A**

### Finding Basis for Column Space
Let **A** be a matrix, with **R** being its *rref* form.
* Basis of Col(**A**) is the nonzero cols of *rref*(**A**) (note: cannot use original matrix **A**, as row operations **do not** preserve column space)

### Rank
Let **A** be an *m* x *n* matrix, and **R** = *rref*(**A**).
* dim(Col(**A**)) = No. of **pivot columns** in **R**  
 = No. of **leading entries** in **R**  
 = No. of **nonzero rows** in **R** = dim(Row(**A**))
* Thus, rank(**A**) = dim(Col(**A**))
* rank(**A**) = rank(**A**<sup>*T*</sup>)
* rank(**A**) $\leq$ min{*m*, *n*}

### Rank-Nullity Theorem (Dimension Theorem)
* rank(**A**) + nullity(**A**) = *n* (no. of columns)

### Null Space Theorem
* Null(**A**) = Null(**A**<sup>*T*</sup>**A**)

### Full Rank
* **A** is full rank if rank(**A**) = min{*m*, *n*}

### Full Rank = *n* (no. of columns)
* rank(**A**) = n
* *Row*(**A**) = $\mathbb{R}^n$
* Columns of **A** are linearly independent
* **Ax** = **0** has only the *trivial solution*, Null(**A**) = {**0**}
* **A**<sup>*T*</sup> is an *invertible matrix* of order *n*
* **A** has a left inverse

### Full Rank = *m* (no. of rows)
* rank(**A**) = *m*
* *Col*(**A**) = $\mathbb{R}^m$
* Rows of **A** are linearly independent
* **Ax** = **b** is consistent for *every* **b** $\in$ $\mathbb{R}^m$
* **AA**<sup>*T*</sup> is an *invertible* matrix of order *m*
* **A** has a right inverse

<div style="page-break-after: always;"></div>

## Orthogonality, Projection, and LSS



## Eigenanalysis

## System of Linear Differential Equations