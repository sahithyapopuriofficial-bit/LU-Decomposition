# LU Decomposition 

## AIM:
To write a program to find L and U matrix And also solve a Matrix using LU Decomposition.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm to find L and U matrix
1. Import required libraries and set OPENBLAS_NUM_THREADS to "1".
2. Read the matrix input from the user and convert it into a NumPy array.
3. Perform LU decomposition using the lu() function to obtain P, L, and U matrices.
4. Print the lower triangular matrix L and upper triangular matrix U.

## Algorithm to solve a matrix using LU Decomposition
1. Import the required libraries and set OPENBLAS_NUM_THREADS to "1".
2. Read the coefficient matrix and constant matrix from the user and convert them into NumPy arrays.
3. Perform LU factorization using lu_factor() and solve the equations using lu_solve().
4. Display the solution vector obtained from the system of linear equations.

## Program:
(i) To find the L and U matrix
```
/*
'''Program to find L and U matrix using LU decomposition.
Developed by: POPURI SAHITHYA
RegisterNumber: 212225240106
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
from scipy.linalg import lu
matrix=np.array(eval(input()))
P,L,U=lu(matrix)
print(L)
print(U)
*/
```

(ii) To find the LU Decomposition of a matrix
```
/*
'''Program to solve a matrix using LU decomposition.
Developed by: POPURI SAHITHYA
RegisterNumber: 212225240106
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
from scipy.linalg import lu_factor,lu_solve
matrix=np.array(eval(input()))
constant=np.array(eval(input()))
piv,lu=lu_factor(matrix)
result=lu_solve((piv,lu),constant)
print(result)
*/
```

## Output:
### L and U Matrix
![alt text](image.png)

### Solving a Matrix using LU Decomposition
![alt text](image-1.png)

## Result:
Thus the program to find L and U Matrix and to solve a Matrix using LU Decomposition is written and verified using python programming.