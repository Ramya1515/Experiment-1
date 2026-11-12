**Experiment 1 — Matrix operations & linear algebra with 
NumPy
**
## AIM

Introduce matrix operations used in ML: transpose, inverse, solve linear systems, eigen decomposition.

## ALGORITHM (Brief)

Direct use of `numpy.linalg` routines; relate to linear regression normal equations.

## PROGRAM

```
import numpy as np
A = np.array([[2.0, 1.0],[1.0, 3.0]])
b = np.array([1.0, 2.0])
print("Matrix A:\n", A)
print("\nTranspose A^T:\n", A.T)
print("\nInverse A^-1:\n", np.linalg.inv(A))
eigvals, eigvecs = np.linalg.eig(A)
print("\nEigenvalues:", np.round(eigvals,4))
x = np.linalg.solve(A,b)
print("\nSolve A x = b --> x:", np.round(x,4))
```

## DETAILED EXPLANATION

1. import numpy as np – Loads NumPy for arrays and linear algebra operations.
2. A = np.array(...) – Defines a 2×2 matrix A.
3. b = np.array(...) – Defines vector b for solving Ax = b.
4. print("Matrix A:", A) – Displays the original matrix for reference.
5. A.T – Computes the transpose by converting rows into columns and columns into rows.
6. np.linalg.inv(A) – Computes the inverse of matrix A. It exists only if the matrix is invertible.
7. np.linalg.eig(A) – Computes eigenvalues and eigenvectors. Eigenvalues help understand variance directions in PCA.
8. np.linalg.solve(A,b) – Numerically solves the linear system Ax = b more stably than `inv(A).dot(b)`.

## SAMPLE OUTPUT

```
Matrix A:
 [[2. 1.]
  [1. 3.]]

Transpose A^T:
 [[2. 1.]
  [1. 3.]]

Inverse A^-1:
 [[ 0.6 -0.2]
  [-0.2  0.4]]

Eigenvalues: [3.618 1.382]

Solve A x = b --> x: [0.2 0.6]
```

## RESULT

Students see concrete matrix computations and how to solve linear systems; relate `solve()` to normal equations in linear regression.

## THEORY

Linear algebra (matrix inversion, eigen-decomposition) underpins PCA, linear models, and many optimization problems. Conditioning and invertibility matter.
