# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Read the order of the system and input the augmented matrix.
2. Perform forward elimination to convert the matrix into upper triangular form.
3. Initialize the last variable using the last row equation.
4.  Apply back substitution to compute remaining variables one by one.
5.   Print the solution values of all variables.
 

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Mithun Kumar V
RegisterNumber: 212225040236

```
```

Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Mithun Kumar V
RegisterNumber: 25012629

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if(a[i][i]==0.0):
        sys.exit("Divide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
    
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=" ")
```

<img width="1536" height="1024" alt="Update program autho" src="https://github.com/user-attachments/assets/2beae415-53f9-4c29-a07f-8aee16a5eae7" />

## Output:
<img width="1186" height="583" alt="522227329-50f9e653-182c-42f5-a3bc-39326db731c0" src="https://github.com/user-attachments/assets/1bc05bed-7ab0-4df6-956a-4f81ae8d5ce3" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

