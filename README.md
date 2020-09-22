# Bregmans-Estimate
import numpy as np

r= int(input('Enter the no of rows'))
c= int(input('Enter the no of colums'))
matrix=[]
for i in range(r):
    row=[]
    for j in range(c):
        ij= int(input())
        row.append(ij)
    matrix.append(row)

print(np.array(matrix))
s= np.sum(matrix, axis=1)
print('row sum : ', s)
value=1
for p in s:
    if p>0:
        fact= np.math.factorial(p)
        fact= fact**(1/p)
        #print(fact)
        value=value*fact
    else: continue
#print(value)
print('Perm(A)<= ', value)
