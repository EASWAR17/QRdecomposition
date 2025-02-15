# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.

## Equipment’s required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Intialize the matrix Q and u

The vector u and e is given by

eqn1

eqn2

eqn3

Obtain the Q matrix
eqn4

Construct the upper triangular matrix R eqn5

## Program:
```
Gram-Schmidt Method
Program to QR decomposition using the Gram-Schmidt method
Developed by:EASWAR J
RegisterNumber: 21002130

import numpy as np
def QR_Decomposition(A):
    n,m = A.shape
    
    Q = np.empty((n,n))
    u = np.empty((n,n))
    
    u[:,0] = A[:,0]
    Q[:,0] = u[:,0]/np.linalg.norm(u[:,0])
    
    for i in range(1,n):
        
        u[:,i] = A[:,i]
        for j in range(i):
            u[:,i] -= (A[:,i] @ Q[:,j]) * Q[:,j]
            
        Q[:,i] = u[:,i]/np.linalg.norm(u[:,i])
        
    R = np.zeros((n,m))
    for i in range(n):
        for j in range(i,m):
            R[i,j] = A[:,j] @ Q[:,i]
    print(Q)
    print(R)
a = np.array(eval(input()))
QR_Decomposition(a)
```
## output:

![mat1](https://user-images.githubusercontent.com/94154683/154698294-2712cf82-c340-4f60-8828-e6e3a6eaf09e.png)

## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
