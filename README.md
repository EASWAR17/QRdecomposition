# Multiplying-two-matrix

## AIM:
To create a program for multiplying  the matrix
## ALGORITHM:

### Step 1:
import numpy as np and give input
### Step 2:
then using loop statement and giving the values
### Step 3:
then finally printing the values


## PROGRAM: 
```
import numpy as np
n =int(input())
l1,l2 = [],[]
for i in range(n):
    l1.append(int(input()))
for i in range(n):
    l2.append(int(input()))
value1 = np.array(l1)
value2 = np.array(l2)
result = value1 *value2
print("Product of two arrays is:",result)

```
## OUTPUT:
![output](s8.png)
![]()
## RESULT:
we succesfully finished th program
