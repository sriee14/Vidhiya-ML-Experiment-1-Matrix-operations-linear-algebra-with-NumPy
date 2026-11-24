## Experiment-1.Matrix operations & linear algebra with NumPy

## AIM:

Introduce matrix operations used in ML: transpose, inverse, solve linear systems, eigen decomposition.

## ALGORITHM:

Direct use of numpy.linalg routines; relate to linear regression normal equations.

## THEORY:

Linear algebra (matrix inversion, eigen-decomposition) underpins PCA, linear models, and many optimization problems. Conditioning/invertibility matters.

## PROGRAM:

```

import numpy as np
A=np.array([[2.0,3.0],[1.0,2.0]])
B=np.array([1.0,2.0])
print("matrix A:\n",A)
print("\nttranspose A^T:\n",A.T)
print("\ninverse A^-1:\n",np.linalg.inv(A))
eigvals,eigvecs=np.linalg.eig(A)
print("\neigenvalues:",np.round(eigvals,4))
x=np.linalg.solve(A,B)
print("\nSolve A x = B --> x:",np.round(x,4))

```

## OUTPUT:

```

matrix A:
 [[2. 3.]
 [1. 2.]]

ttranspose A^T:
 [[2. 1.]
 [3. 2.]]

inverse A^-1:
 [[ 2. -3.]
 [-1.  2.]]

eigenvalues: [3.7321 0.2679]

Solve A x = B --> x: [-4.  3.]

```

## RESULT:

Students see concrete matrix computations and how to solve linear systems; relate solve() to normal equations in linear regression.
