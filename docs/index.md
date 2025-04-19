---
layout: default
title: MA1508E
---

# MA1508E Formulae, Theorems and Definitions

## Table of Contents

1. **[Chapter 1: Linear Systems](#linear-systems)**
2. **[Chapter 2: Matrix Algebra](#matrix-algebra)**
3. **[Chapter 3: Euclidean Vector Spaces](#euclidean-vector-spaces)**
4. **[Chapter 4: Subspaces Associated to a Matrix](#subspaces)**
5. **[Chapter 5: Orthogonality, Projection, and Least Square Solution](#orthogonality-projection-and-lss)**
6. **[Chapter 6: Eigenanalysis](#eigenanalysis)**
7. **[Chapter 7: System of Linear Differential Equations](#system-of-linear-differential-equations)**

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

* (**A**<suP>T</sup>)<sup>T</sup> = **A**
* (_c_**A**)<sup>T</sup> = _c_**A**<sup>T</sup>
* (**A** + **B**)<sup>T</sup>= **A**<sup>T</sup> + **B**<sup>T</sup>
* (**AB**)<sup>T</sup> = **B**<sup>T</sup>**A**<sup>T</sup>
* If **A** is **symmetric**, **A**<sup>T</sup> = **A**

### Block Multiplication

* 
```math
AB = A \begin{pmatrix} \mathbf{b}_1 & \mathbf{b}_2 & \cdots & \mathbf{b}_n \end{pmatrix} = \begin{pmatrix} A\mathbf{b}_1 & A\mathbf{b}_2 & \cdots & A\mathbf{b}_n \end{pmatrix}
```
* 
```math
AB = \begin{pmatrix}
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
```

### Invertible Matrices

[Final Invertible List](...)

### Properties of Invertible Matrices

Let **A** be an invertible matrix of order n.

* (**A**<sup>-1</sup>)<sup>-1</sup> = **A**
* (*a***A**)<sup>-1</sup> = $\frac{1}{a}$**A**<sup>-1</sup>
* (**A**<sup>T</sup>)<sup>-1</sup> = (**A**<sup>-1</sup>)<sup>T</sup>
* (**AB**)<sup>-1</sup> = **B**<sup>-1</sup>**A**<sup>-1</sup>

### Elementary Matrices

* If **B** is row equivalent to **A**, **B** = **E<sub>k</sub>...E<sub>2</sub>E<sub>1</sub>A**.

### Inverse of Elementary Matrices

* **E**: *R<sub>i</sub>* + *cR<sub>j</sub>*, **E<sup>-1</sup>**: *R<sub>i</sub>* - *cR<sub>j</sub>*
* **E**: *R<sub>i</sub>* ↔ *R<sub>j</sub>*, **E**<sup>-1</sup>: *R<sub>i</sub>* ↔ *R<sub>j</sub>* (same matrix!)
* **E**: *cR<sub>i</sub>*, **E**<sup>-1</sup>: $$\frac{1}{c}$$*R<sub>i</sub>*

### Determinant

* For 2x2 matrices, $\mathbf{A} = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, $\det(\mathbf{A}) = ad - bc$.
* For higher powers, use cofactor expansion:
    1. `$\begin{pmatrix}
       \text{+} & \text{-} & \text{+} & \cdots & \cdots \\
       \text{-} & \text{+} & \text{-} & \cdots & \cdots \\
       \text{+} & \text{-} & \text{+} & \cdots & \cdots \\
       \vdots & \vdots & \vdots & \ddots & \vdots \\
       \cdots & \cdots & \cdots & \cdots & \cdot
       \end{pmatrix}$` (Remember to check the sign!)

### Properties of Determinant

Let **A** be a square matrix.

* det(**A**) = det(**A**<sup>T</sup>)
* If **A** is triangular, det(**A**) = *a<sub>11</sub>a<sub>22</sub>...a<sub>nn</sub>*
    * Multiply all its diagonal entries

### Determinant of Elementary Row Operations

* **E**: *R<sub>i</sub>* + *cR<sub>i</sub>* → det(**E**) = 1
* **E**: *R<sub>i</sub>* ↔ *R<sub>i</sub>* → det(**E**) = -1
* **E**: *cR<sub>i</sub>* → det(**E**) = c

## Euclidean Vector Spaces

## Subspaces

## Orthogonality, Projection, and LSS

## Eigenanalysis

## System of Linear Differential Equations