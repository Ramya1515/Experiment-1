
# EXPERIMENT 1 – MATRIX OPERATIONS AND LINEAR ALGEBRA USING NUMPY

## AIM
To introduce matrix operations used in Machine Learning, including transpose, inverse, solving linear systems, and eigenvalue decomposition using NumPy.

## ALGORITHM
1. Import the NumPy library.
2. Define a 2×2 matrix A and a vector b.
3. Display the original matrix.
4. Calculate the transpose of matrix A.
5. Find the inverse of matrix A.
6. Calculate the eigenvalues and eigenvectors.
7. Solve the linear equation Ax = b using NumPy.
8. Display all the results.

## PROGRAM

```python
import numpy as np

A = np.array([[2.0, 1.0],
              [1.0, 3.0]])

b = np.array([1.0, 2.0])

print("Matrix A:\n", A)

print("\nTranspose A^T:\n", A.T)

print("\nInverse A^-1:\n", np.linalg.inv(A))

eigvals, eigvecs = np.linalg.eig(A)
print("\nEigenvalues:", np.round(eigvals, 4))

x = np.linalg.solve(A, b)
print("\nSolve A x = b --> x:", np.round(x, 4))
```

## SAMPLE OUTPUT

```text
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

## DETAILED EXPLANATION

1. **import numpy as np** – Imports NumPy for numerical operations and matrix calculations.
2. **A = np.array()** – Defines a 2×2 matrix A.
3. **b = np.array()** – Defines a vector b for solving Ax = b.
4. **print()** – Displays the original matrix.
5. **A.T** – Calculates the transpose by interchanging rows and columns.
6. **np.linalg.inv(A)** – Calculates the inverse of matrix A.
7. **np.linalg.eig(A)** – Calculates eigenvalues and eigenvectors.
8. **np.linalg.solve(A, b)** – Solves the linear system Ax = b.

## RESULT

Thus, matrix operations such as transpose, inverse, eigenvalue decomposition and solving linear equations were successfully performed using NumPy.

## THEORY

Linear algebra is an important foundation of Machine Learning. Matrix operations are used in linear regression, Principal Component Analysis (PCA), and optimization problems.
