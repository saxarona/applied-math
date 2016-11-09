# Notes on the Symmetric Eigenvalues Problem

## Eigenvalues and Eigenvectors

This is the characteristic polynomial:

````p(x) = det(A - xI)````

Where `A` is a square matrix.

The roots of the characteristic polynomial are called the *eigenvalues* of `A`. The set of `A`'s eigenvalues is

````\gamma (A) = \{x: det(A - xI) = 0\}````

An `n`-by-`n` matrix has `n` eigenvalues.

If the eigenvalues of `A` are real, they are usually indexed from largest to smallest:

````\gamma_n(A) \leq \dots \leq ````

If `X` is a square matrix, and it is non-singular (i.e. it has an inverse matrix), and `B = X^{-1} AX`, then `A` and `B` are *similar*.
If two matrices are similar, then they have exactly the same eigenvalues.

If `\gamma \in \gamma (A)`, then there exists a nonzero vector `x` so that `Ax = \gamma x`. This `x` vector is said to be an *eigenvector* for `A` associated with `\gamma`.

## Positive definite system

A square, real matrix `A` is *positive definite* if `x^T A x > 0` for all nonzero `x \in \mathbb{R}^n`.
It is called *positive semidefinite* if it is greater or equal than 0, or indefinite if `x,y \in \mathbb{R}^n` so that `(x^T Ax)(y^T Ay) < 0.

A positive definite matrix `A` is nonsingular, i.e. there exists an inverse `A^{-1}`


Intel definition:

> Symmetric eigenvalue problems are posed as follows: given an n-by-n real symmetric or complex Hermitian matrix A, find the eigenvalues λ and the corresponding eigenvectors z that satisfy the equation Az = λz (or, equivalently, zHA = λzH).


T is tridiagonal matrix, i.e.

[T11, T12,  0 ]
[T21, T22, T23]
[ 0 , T32, T33]

## Unitary Matrices

Over the complex field, the unitary matrices correspond to the orthogonal matrices.
A matrix `Q` which is square and complex is unitary if `Q^H Q = Q Q^H = I_n`

Unitary transformations preserve 2-norm and Frobenius norm.

If `A` is a non-square complex matrix, then there exists unitary matrices `U \in \mathbb{C}^{n \times n}` and `V \in \mathbb{C}^{m \times m}` such that `U^H A V = diag(\delta_1 , \dots , \delta_p) \in \mathbb{R}^{m \times n}` with `p=\text{min}{m,n}`.

## QR Factorization

If `A \in \mathbb{R}^{m \times n}`, then there exists an orthogonal `Q` which is real and square with `m` rows, and an upper triangular `R` with `m` rows and `n` columns so that `A = QR`.

## SVD

The Singular Value decomposition is an orthogonal matrix reduction.

If `A` is a real `m`-by-`n` matrix, then there exists orthogonal matrices U and V (both square, `m`-by-`m` and `n`-by-`n` respectively) such that `U^T A V = diag(\sigma_1 , \dots , \sigma_p) \in \mathbb{R}^{m \times n}, p = \text{min}{m,n}` where `\sigma_1 \geq \sigma_2 \geq \dots \geq \sigma_p \geq 0`.

##Schur decomposition

If `A` \in `\mathbb{R}^{n \times n}` is symmetric, then there exists an orthogonal `Q` so that `Q^T A Q = \text{diag}(\lambda_1, \dots, \lambda_n)`.


## Presentation Outline

- Eigenvalues and eigenvectors
- QR factorization
- The symmetric eigenvalues problem
	- 8.7
	- Symmetric-Definite Generalized Eigenproblem
- Some properties
- Law of Inertia
- Some Power Iterations
- Reduction to Tridiag
- QR and Tridiag
- Eigenvalues by bisection
- Sturm Sequence
- Classic Jacobi
- SVD and SEP
- SVD algorithm
- Quadratic Eigenvalue Problem
510