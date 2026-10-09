## DATE:  28/08/2026








 

## AIM









Introduce matrix operations used in ML: transpose, inverse, solve linear systems, eigen decomposition. 








## THEORY:







Linear algebra (matrix inversion, eigen-decomposition) underpins PCA, linear models, and many optimization problems. Conditioning/invertibility matters. 










## ALGORITHM :






 
Direct use of numpy.linalg routines; relate to linear regression normal equations.









## PROGRAM 


















```

import numpy as np
import pandas as pd
A= np.array([[2.0,1.0],[1.0,3.0]])
B= np.array([1.0,2.0])
print ("matrix A:\n",A)
print ("\ntranspose A^T:\n",A.T)
print("\ninverse A^-1:\n", np.linalg.inv(A))
eigvals, eigvecs = np.linalg.eig(A)
print("\nEigenvalues:", np.round(eigvals ,4))
x= np.linalg.solve(A,B)
print ("\nsolve A x = B--> x:",np.round(x,4))


```















## OUTPUT
















```

matrix A:
 [[2. 1.]
 [1. 3.]]

transpose A^T:
 [[2. 1.]
 [1. 3.]]

inverse A^-1:
 [[ 0.6 -0.2]
 [-0.2  0.4]]

Eigenvalues: [1.382 3.618]

solve A x = B--> x: [0.2 0.6]

```






## RESULT: 




















Students see concrete matrix computations and how to solve linear systems; relate solve() to normal equations in linear regression. 
