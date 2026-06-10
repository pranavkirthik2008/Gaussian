# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: PRANAV KIRTHIK S S <img width="1232" height="580" alt="595987497-300d3d33-3ec9-4524-bb43-1a031fa182a2" src="https://github.com/user-attachments/assets/f2421664-0603-4b2b-9c5c-a9b128abd945" />

RegisterNumber:212222530212
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
import numpy as np
n=int(input())
a=np.zeros((n,n+1))
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    for j in range(i+1,n):
        ratio = a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio * a[i][k]
x=np.zeros(n)
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print("X%d = %0.2f" % (i,x[i]),end=" ")

*/
```

## Output:
<img width="1232" height="580" alt="595987497-300d3d33-3ec9-4524-bb43-1a031fa182a2" src="https://github.com/user-attachments/assets/42d7f6e8-5d6e-4cd1-b58e-4c285d5b3e14" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

